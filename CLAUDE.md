# khairulislam.github.io

Jekyll site (Minimal Mistakes-based theme) for a GitHub Pages academic homepage.

## Local build/preview (HPC cluster, no sudo)

Ruby isn't on PATH by default; a `ruby/3.4.3` environment module is available.

```bash
module load ruby/3.4.3
export PATH="$HOME/.local/share/gem/ruby/3.4.0/bin:$PATH"   # bundler install location
bundle config set --local path 'vendor/bundle'                # first time only
bundle install
bundle exec jekyll build      # outputs to _site/
```

**Never pipe `module load`.** `module` is a shell function; a pipe runs it in a
subshell, so the PATH it exports is discarded and the module appears not to
load. This is silent: no error, no output, `ruby` simply stays missing.

```bash
module load ruby/3.4.3 2>/dev/null        # works (redirect)
module load ruby/3.4.3 2>&1 | tail -2     # NO-OP, ruby still not on PATH
```

The same applies to `eval "$($LMOD_CMD bash load ruby/3.4.3)"` if the eval is
piped anywhere. Redirect instead of piping, then verify on its own line with
`ruby -v`. If ruby is missing right after a "successful" load, suspect a pipe
before suspecting the cluster.

**Don't `tail` a `module avail` check.** Lmod prints a multi-line help footer,
so `module avail ruby 2>&1 | tail -10` shows only that footer and makes an
available module look deleted. Use `module avail ruby 2>&1 | grep ruby`.

The module is real and current; if it looks gone, re-check with grep before
reaching for the install path directly
(`/apps/software/standard/core/ruby/3.4.3/bin`, also reachable through
`/sfs/gpfs/tardis/applications/202606/...`). Loading `miniforge` first makes no
difference and is not needed.

`vendor/bundle` and `_site` are build artifacts — not committed.

A plain build like the one above links every stylesheet to the **live** site.
Never inspect or screenshot local CSS work from it; add the `url: ""` override
in "Screenshotting the built site locally" below. A computed size that matches
the old theme rather than your edit is the classic symptom.

**Known issue:** the `hawkins` gem (live-reload for `jekyll serve`) pulls in
`eventmachine`, which fails to load on this cluster (`libssl.so.3: cannot open
shared object file`). `bundle exec jekyll build` now hits this too, since
Bundler requires every gem in the group before Jekyll runs — plain builds do
*not* work as-is. Build against a copy of the Gemfile with the `hawkins` line
removed instead of fighting the missing system lib:

```bash
grep -v hawkins Gemfile > /tmp/Gemfile.nolive
cp Gemfile.lock /tmp/Gemfile.nolive.lock  # reuse the resolved versions
BUNDLE_GEMFILE=/tmp/Gemfile.nolive bundle install   # first time only
BUNDLE_GEMFILE=/tmp/Gemfile.nolive BUNDLE_PATH="$PWD/vendor/bundle" \
  bundle exec jekyll build
```

`BUNDLE_PATH` must be **absolute** here. The repo's `.bundle/config` sets a
relative `vendor/bundle`, which Bundler resolves against the *Gemfile's*
directory, so a Gemfile in `/tmp` looks for `/tmp/vendor/bundle` and fails with
the misleading `bundler: command not found: jekyll` /
`Install missing gem executables with 'bundle install'`. That message means the
path is wrong, not that gems are missing.

## Screenshotting the built site locally

- **Build with `url: ""` or the screenshot is of production, not your work.**
  `_config.yml` sets `url: https://khairulislam.github.io`, and the theme builds
  absolute asset paths from it, so a default build's pages pull CSS from the
  *live site* even when served from localhost. Local CSS edits then appear to do
  nothing, and — worse — the page still looks styled, so nothing signals the
  problem. Override it at build time:
  `bundle exec jekyll build --config _config.yml,local.yml` with
  `url: ""` / `baseurl: ""` in `local.yml`. Verify before trusting a screenshot:
  `chromium-browser --headless=new --dump-dom URL | grep 'rel="stylesheet"'`
  must show `/assets/...`, not `https://khairulislam.github.io/assets/...`.
- `python3 -m http.server` is single-threaded and can stall when a browser
  opens many concurrent connections for a page's assets — serve `_site/`
  with a threaded server instead (`http.server.ThreadingHTTPServer`).
- Restart that server after any `rm -rf _site && jekyll build`. It resolves
  requests against its original working directory, which a rebuild replaces
  with a new inode, so every request 404s until it is restarted.
- Headless `chromium-browser` (`--headless=new --disable-gpu --no-sandbox
  --window-size=W,H --screenshot=out.png URL`) on this machine has a
  software-rasterizer bug: any page using this theme's CSS `intro` fade-in
  keyframe animation (`_sass/_animations.scss`, used on `.masthead` and
  `#main` via `_sass/_page.scss`) screenshots as **entirely blank** — even
  the live production site reproduces it, so it is not a sign of broken
  code. Work around it by neutralizing animations before screenshotting,
  e.g. inject `<style>*{animation:none !important;transition:none
  !important}</style>` before `</head>` in the built HTML, then screenshot
  normally.

## Styling the archive pages (`layout: archive`)

`/publications/`, `/teaching/`, `/cv/`, `/awards/` and `/education/` render
through `_layouts/archive.html`, which wraps content in `<div class="archive">`
and has **no `.page__content` element at all**. Only `_layouts/single.html`
has `.page__content`, which is what the homepage gets (via the `_pages` default
`layout: single` in `_config.yml`, not a front-matter key in `about.md`).

So a rule written as `.page__content .archive__item p { ... }` silently applies
to nothing on exactly the pages it names. Nothing errors; the page just keeps
the old size. Put archive typography in `_sass/_archive.scss` scoped to
`.archive__item` / `.cv__item` without a `.page__content` prefix.

Before trusting a CSS change on these pages, confirm the rule actually matched
rather than eyeballing a screenshot:

```bash
# after building and serving _site/
chromium-browser --headless=new --disable-gpu --no-sandbox \
  --virtual-time-budget=2000 --dump-dom http://127.0.0.1:PORT/publications/
```

with a small `<script>` appended to the built HTML that writes
`getComputedStyle(el)` values into `document.title`. A computed value that
still shows the theme default means the selector missed.

Site-wide type scale lives in the root `font-size` in `_sass/_reset.scss`.
Nearly everything else in the theme is `em`/`rem`, so that one declaration
scales every page at once. Upstream Minimal Mistakes bumps it from 16px to 18px
at the `$medium` breakpoint; that bump is deliberately removed here, so the
root stays a flat 16px. Adjust site-wide size there rather than page by page,
and don't reintroduce the breakpoint bump.

## Liquid gotchas

`post.excerpt` is **whitespace, not nil**, for a collection entry with no body
(most publications). Whitespace is truthy in Liquid, so `{% if post.excerpt %}`
renders an empty `<p class="archive__item-excerpt">` that still carries a
paragraph margin and opens a dead gap under every entry. Test the stripped
text: `{% assign t = post.excerpt | strip_html | strip %}{% if t != '' %}`.

Includes wrapped in a `<ul>` by their caller (`archive-single-cv.html`, used by
`_pages/cv.md`) must emit the `<li>` as their outermost element. A
`<div>`/`<article>` between `<ul>` and `<li>` is invalid nesting and renders as
stray bullets and boxes.

## Content hygiene

The unused AcademicPages demo content (`/talks/`, `/portfolio/`, `/markdown/`,
`/non-menu-page/`, `/terms/`, the archive samples, the "Blog Post number N"
posts, `talkmap/`) is listed under `exclude:` in `_config.yml`. It was unlinked
from the nav but still built, served and listed in `sitemap.xml`. Keep it
excluded; don't re-add pages from the upstream template without checking what
they publish. `CLAUDE.md` and `markdown_generator/` are excluded for the same
reason: both were publicly reachable.

Excluding *individual files* inside a directory named in `include:` breaks the
whole directory. Listing `files/paper1.pdf` under `exclude:` stopped `files/`
publishing entirely, including files that were not excluded. Exclude the
directory or delete its contents; don't mix the two. (`files/` has since been
deleted and dropped from `include:`.)

## Writing rules
* No '—' unless necessary
* Avoid marketting, overclaim, unverified statements.