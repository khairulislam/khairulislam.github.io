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

`vendor/bundle` and `_site` are build artifacts — not committed.

**Known issue:** the `hawkins` gem (live-reload for `jekyll serve`) pulls in
`eventmachine`, which fails to load on this cluster (`libssl.so.3: cannot open
shared object file`). It's unused for local review — `jekyll build` alone
doesn't hit this path, so plain builds work fine. If `jekyll serve`/live-reload
is needed, use a Gemfile without the `hawkins` group instead of fighting the
missing system lib.

## Screenshotting the built site locally

- `python3 -m http.server` is single-threaded and can stall when a browser
  opens many concurrent connections for a page's assets — serve `_site/`
  with a threaded server instead (`http.server.ThreadingHTTPServer`).
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

## Writing rules
* No '—' unless necessary
* Avoid marketting, overclaim, unverified statements.