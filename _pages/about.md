---
permalink: /
title: "Homepage"
hide_page_title: true
description: "I design generative and foundation models for scientific data, built to run without a supercomputer and to transfer across instruments and domains."
redirect_from: 
  - /about/
  - /about.html
---

<div class="hp-profile">
<div class="hp-profile-main">
<h1 class="hp-name">{{ site.author.name }}</h1>
<p class="hp-title"><span class="hp-role">{{ site.author.bio }}</span><span class="hp-location"><i class="fas fa-location-dot" aria-hidden="true"></i>{{ site.author.location }}</span></p>

<div class="hp-bio" markdown="1">
I design Generative AI and Foundation models for scientific data, to run efficiently at high resolutions and to unify across representations. I am a sixth-year Computer Science Ph.D. candidate at the [University of Virginia](https://engineering.virginia.edu/department/computer-science), advised by [Professor Judy Fox](https://judyfox.online/) and co-advised by [Professor Geoffrey Fox](https://engineering.virginia.edu/faculty/geoffrey-c-fox).

My research spans **Generative AI** ([Cosmo3DFlow](https://dl.acm.org/doi/10.1145/3770855.3818994), KDD 2026, wavelet flow matching for efficient 3D reconstruction, creates $128^3$ in seconds vs minute in Diffusion, scales to $1024^3$), **Unified Foundation Model** ([OmniSpectra](https://arxiv.org/pdf/2601.15351), unifies representation across millions of spectra with different lengths and resolutions), **Explainable AI** ([WinTSR](https://arxiv.org/pdf/2412.04532), AAAI 2025 AI4TS workshop, interpreting temporal patterns over context windows), **Scalable AI** ([AI Inference](https://journals.sagepub.com/doi/full/10.1177/10943420251399942), IJHPCA 2025, serverless computing for ViT inference on AWS Cloud container). My xAI work on time series have been awarded **First Place** in the [2024 CIC Student Paper Challenge](https://covidinfocommons.datascience.columbia.edu/content/2024-cic-student-paper-challenge) for [Interpreting time series sensitivity](https://arxiv.org/html/2401.15119v1), **Third Place** at the [NSF Student Research Competition, ICDH 2023](https://conferences.computer.org/icdh/2023/student_awards.html) for interpreting [Spatio-temporal attention patterns](https://ieeexplore.ieee.org/abstract/document/10224685).

I often participate in Kaggle ML competitions and have **2 Silver** and **2 Bronze** medals there (currently ranked **3,225 worldwide, top 1.5%**). My opensource works include: [tslens](https://github.com/khairulislam/tslens), PyTorch library for interpreting SOTA time series models (traditional & foundation); [Financial Time Series using LLMs](https://github.com/UVA-MLSys/Financial-Time-Series); [Astronomy Vision](https://github.com/khairulislam/VLASS-Vision); [Anomaly Detection](https://github.com/khairulislam/Anomaly-Detection-on-UNSW-NB15). Before UVA, I spent two years as an iOS software developer at [Samsung Research, Bangladesh](https://research.samsung.com/srbd) (2018–2020), after a B.Sc. from [Bangladesh University of Engineering and Technology](https://cse.buet.ac.bd/). I assisted in teaching for several courses at UVA (see [Teaching](/teaching/)). In my spare time I enjoy Chess and Table Tennis. **I am on the job market and available from Spring 2027.** If you would like to talk research or explore working together, [reach out](mailto:{{ site.author.email }}).
</div>

<div class="hp-social-row">
<a href="mailto:{{ site.author.email }}" title="Email" aria-label="Email"><i class="fas fa-envelope" aria-hidden="true"></i></a>
<a href="{{ site.author.googlescholar }}" title="Google Scholar" aria-label="Google Scholar"><i class="ai ai-google-scholar" aria-hidden="true"></i></a>
<a href="{{ site.author.orcid }}" title="ORCID" aria-label="ORCID"><i class="ai ai-orcid" aria-hidden="true"></i></a>
<a href="https://github.com/{{ site.author.github }}" title="GitHub" aria-label="GitHub"><i class="fab fa-github" aria-hidden="true"></i></a>
<a href="https://kaggle.com/{{ site.author.kaggle }}" title="Kaggle" aria-label="Kaggle"><i class="fab fa-kaggle" aria-hidden="true"></i></a>
<a href="https://linkedin.com/in/{{ site.author.linkedin }}" title="LinkedIn" aria-label="LinkedIn"><i class="fab fa-linkedin" aria-hidden="true"></i></a>
</div>
</div>

<div class="hp-profile-photo">
<img src="/images/{{ site.author.avatar }}" alt="{{ site.author.name }}">
</div>
</div>

<section class="hp-section">
<h2 class="hp-heading">News</h2>

<ul class="hp-news-list" id="hp-news-list">
  <li class="hp-news-item"><span class="hp-news-date">Aug 2026</span><span class="hp-news-text">Released <a href="https://github.com/khairulislam/tslens">tslens</a> on PyPI: a PyTorch library unifying 15+ attribution methods across 25+ time series architectures.</span></li>
  <li class="hp-news-item"><span class="hp-news-date">Jul 2026</span><span class="hp-news-text">Passed my Ph.D. Proposal exam. Title: <em>"Generative and Foundation Models for Scientific Data"</em>.</span></li>
  <li class="hp-news-item"><span class="hp-news-date">Jun 2026</span><span class="hp-news-text"><strong>Bronze Medal</strong> (top 10%, 279th of 3677 teams) in the <a href="https://www.kaggle.com/competitions/hull-tactical-market-prediction">Hull Tactical Market Prediction</a> Kaggle competition.</span></li>
  <li class="hp-news-item"><span class="hp-news-date">May 2026</span><span class="hp-news-text"><a href="https://dl.acm.org/doi/10.1145/3770855.3818994">Cosmo3DFlow</a> accepted at <strong>KDD 2026</strong>, sampling with an order of magnitude fewer integration steps than diffusion models. <a href="https://github.com/UVA-MLSys/Cosmo3DFlow">Code</a>.</span></li>
  <li class="hp-news-item"><span class="hp-news-date">Jan 2026</span><span class="hp-news-text">Preprint: <a href="https://arxiv.org/pdf/2601.15351">OmniSpectra: A Unified Foundation Model for Universal Spectra Representation Learning</a>.</span></li>
  <li class="hp-news-item"><span class="hp-news-date">Jan 2026</span><span class="hp-news-text">TA for <a href="https://www.cs3240.org/">Software Engineering (CS 3240)</a>, instructors Prof. Mark Sherriff and Prof. Sarah Elder.</span></li>
  <li class="hp-news-item"><span class="hp-news-date">Nov 2025</span><span class="hp-news-text"><a href="https://journals.sagepub.com/doi/full/10.1177/10943420251399942">Scalable Cosmic AI Inference using Cloud Serverless Computing</a> accepted at the <strong>International Journal of High Performance Computing Applications</strong>. <a href="https://github.com/UVA-MLSys/AI-for-Astronomy">Code</a>.</span></li>

  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">Aug 2025</span><span class="hp-news-text">TA for <a href="https://www.cs3240.org/">Software Engineering (CS 3240)</a>, instructor Prof. Mark Sherriff.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">Jul 2025</span><span class="hp-news-text"><strong>Silver Medal</strong> (top 5%, 155th of 3757 teams) in the <a href="https://www.kaggle.com/competitions/jane-street-real-time-market-data-forecasting">Jane Street Real-Time Market Data Forecasting</a> Kaggle competition.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">May 2025</span><span class="hp-news-text">TA for <a href="https://github.com/UVA-MLSys/DS5110_Summer_2025">Big Data Systems (DS 5110)</a>, instructor Prof. Judy Fox.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">Jan 2025</span><span class="hp-news-text">TA for <a href="https://mz8rr.github.io/FoDA/schedule.html">Foundations of Data Analysis (CS 3501 / ECE 3502)</a>, instructor Prof. Miaomiao Zhang.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">Dec 2024</span><span class="hp-news-text"><a href="https://arxiv.org/pdf/2412.04532">WinTSR</a> accepted at the <strong>AAAI 2025</strong> Workshop on AI for Time Series Analysis.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">Nov 2024</span><span class="hp-news-text">Featured in UVA Engineering news, <a href="https://engineering.virginia.edu/news-events/news/uva-phd-student-uncovers-covid-19-transmission-patterns">UVA Ph.D. student uncovers COVID-19 transmission patterns</a>.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">Nov 2024</span><span class="hp-news-text">"Large Language Models for Financial Aid in Financial Time-series Forecasting" accepted at the <a href="https://intelligentfinance.github.io/IEEE-LLM-finance-2024/index.html">IEEE BigData 2024 Workshop on LLMs for Finance</a>.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">Oct 2024</span><span class="hp-news-text">Started astronomy research with <strong>NRAO</strong> (National Radio Astronomy Observatory) through the <a href="https://new.nsf.gov/news/nsf-simons-foundation-launch-2-ai-institutes-help">NSF–Simons AI Institute</a>.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">Sep 2024</span><span class="hp-news-text"><strong>First Place</strong> in the <a href="https://covidinfocommons.datascience.columbia.edu/content/2024-cic-student-paper-challenge">2024 COVID Information Commons Student Paper Challenge</a> (graduate cohort), organized by Columbia University, for <a href="/publication/2024-03-27">"Interpreting Time Series Transformer Models and Sensitivity Analysis of Population Age Groups to COVID-19 Infections"</a>.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">Aug 2024</span><span class="hp-news-text">TA for <a href="https://kunqian.info/teaching/uva_cs6501_ws4iot/fall2024/">Wireless Sensing for IoT (CS 6501)</a>.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">May 2024</span><span class="hp-news-text">Graduated from UVA with a Master's (en route) degree in Computer Science.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">Dec 2023</span><span class="hp-news-text"><a href="https://arxiv.org/html/2401.15119v1">Interpreting Time Series Transformer Models and Sensitivity Analysis of Population Age Groups to COVID-19 Infections</a> accepted at the <strong>AAAI 2024</strong> Workshop on AI for Time Series Analysis. The paper later won <strong>First Place</strong> in the 2024 COVID Information Commons Student Paper Challenge.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">Nov 2023</span><span class="hp-news-text">Passed my Ph.D. qualifier exam on interpreting time series models by explicitly accounting for temporal importance.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">Oct 2023</span><span class="hp-news-text"><a href="https://ojs.aaai.org/index.php/AAAI/article/view/30396">Temporal Dependencies and Spatio-Temporal Patterns of Time Series Models</a> accepted at the <strong>AAAI/SIGAI Doctoral Consortium 2024</strong>.</span></li>
  <li class="hp-news-item hp-news-hidden"><span class="hp-news-date">Jul 2023</span><span class="hp-news-text"><strong>Third Place</strong> in the <a href="https://conferences.computer.org/icdh/2023/student_awards.html">NSF Student Research Competition</a> at the IEEE International Conference on Digital Health, for <a href="/publication/2023-07-08">"Interpreting County-Level COVID-19 Infections using Transformer and Deep Learning Time Series Models"</a>.</span></li>
</ul>

<button class="hp-news-toggle" id="hp-news-toggle" type="button" aria-expanded="false">Show more</button>
</section>

<section class="hp-section">
<h2 class="hp-heading">Selected Publications</h2>

<div class="hp-pub-group">
  <div class="hp-pub-label">Generative &amp; Foundation Models for Science</div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">Cosmo3DFlow: Wavelet Flow Matching for Spatial-to-Spectral Compression in Reconstructing the Early Universe</div>
    <div class="hp-pub-authors"><strong>Md Khairul Islam</strong>, Zeyu Xia, Ryan Goudjil, Jialu Wang, Arya Farahi, Judy Fox</div>
    <div class="hp-pub-venue">KDD 2026</div>
    <div class="hp-pub-desc">Combines 3D wavelet transforms with flow matching to reconstruct the early universe from cosmological simulations, cutting diffusion-model sampling cost by 46×.</div>
    <div class="hp-pub-links">
      <a href="https://dl.acm.org/doi/10.1145/3770855.3818994">Paper</a>
      <a href="https://github.com/UVA-MLSys/Cosmo3DFlow">Code</a>
    </div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">OmniSpectra: A Unified Foundation Model for Universal Spectra Representation Learning</div>
    <div class="hp-pub-authors"><strong>Md Khairul Islam</strong>, et al.</div>
    <div class="hp-pub-venue">Preprint, 2026</div>
    <div class="hp-pub-desc">A single foundation model for spectra across instruments, handling variable-length inputs at native resolution without resampling.</div>
    <div class="hp-pub-links">
      <a href="https://arxiv.org/pdf/2601.15351">Paper</a>
    </div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">Scalable Cosmic AI Inference using Cloud Serverless Computing</div>
    <div class="hp-pub-authors">Mills Staylor, Amirreza Dolatpour Fathkouhi, <strong>Md Khairul Islam</strong>, et al.</div>
    <div class="hp-pub-venue">IJHPCA 2025</div>
    <div class="hp-pub-desc">A cloud framework combining pretrained models with serverless infrastructure to run deep-learning astronomical inference without dedicated HPC access.</div>
    <div class="hp-pub-links">
      <a href="https://journals.sagepub.com/doi/full/10.1177/10943420251399942">Paper</a>
      <a href="https://github.com/UVA-MLSys/AI-for-Astronomy">Code</a>
    </div>
  </div>
</div>

<div class="hp-pub-group">
  <div class="hp-pub-label">Explainable Time Series Deep Learning</div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">WinTSR: A Windowed Temporal Saliency Rescaling Method for Interpreting Time Series Deep Learning Models</div>
    <div class="hp-pub-authors"><strong>Md Khairul Islam</strong>, Judy Fox</div>
    <div class="hp-pub-venue">AAAI 2025 Workshop (AI4TS)</div>
    <div class="hp-pub-desc">A windowed saliency method that captures delayed temporal dependencies, outperforming prior interpretation techniques across multiple architectures and datasets.</div>
    <div class="hp-pub-links">
      <a href="https://arxiv.org/pdf/2412.04532">Paper</a>
      <a href="https://github.com/khairulislam/Timeseries-Explained">Code</a>
    </div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">Interpreting Time Series Transformer Models and Sensitivity Analysis of Population Age Groups to COVID-19 Infections</div>
    <div class="hp-pub-authors"><strong>Md Khairul Islam</strong>, Judy Fox</div>
    <div class="hp-pub-venue">AAAI 2024 Workshop (AI4TS)</div>
    <div class="hp-pub-award">First Place, 2024 COVID Information Commons Student Paper Challenge (graduate cohort)</div>
    <div class="hp-pub-desc">Benchmarks eight interpretation methods across six transformer models using 3.5M COVID-19 case records to identify which age groups drove transmission.</div>
    <div class="hp-pub-links">
      <a href="https://arxiv.org/html/2401.15119v1">Paper</a>
    </div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">Temporal Dependencies and Spatio-Temporal Patterns of Time Series Models</div>
    <div class="hp-pub-authors"><strong>Md Khairul Islam</strong>, Judy Fox</div>
    <div class="hp-pub-venue">AAAI/SIGAI Doctoral Consortium 2024</div>
    <div class="hp-pub-desc">Doctoral consortium work on explicitly modeling temporal importance to produce more precise explanations of feature interactions in time series models.</div>
    <div class="hp-pub-links">
      <a href="https://ojs.aaai.org/index.php/AAAI/article/view/30396">Paper</a>
      <a href="https://github.com/UVA-MLSys/SA-Timeseries">Code</a>
    </div>
  </div>
</div>

<a class="hp-view-all" href="/publications/">See all publications →</a>
</section>

<section class="hp-section">
<h2 class="hp-heading">Awards</h2>

<div class="hp-pub-group">
  <div class="hp-pub-label">Paper Awards</div>
  <ul class="hp-news-list">
    <li class="hp-news-item"><span class="hp-news-date">Sep 2024</span><span class="hp-news-text"><strong>First Place</strong> (graduate cohort) in the <a href="https://covidinfocommons.datascience.columbia.edu/content/2024-cic-student-paper-challenge">2024 COVID Information Commons Student Paper Challenge</a>, Columbia University, for <a href="/publication/2024-03-27">"Interpreting Time Series Transformer Models and Sensitivity Analysis of Population Age Groups to COVID-19 Infections"</a>.</span></li>
    <li class="hp-news-item"><span class="hp-news-date">Jul 2023</span><span class="hp-news-text"><strong>Third Place</strong> in the <a href="https://conferences.computer.org/icdh/2023/student_awards.html">NSF Student Research Competition</a>, IEEE International Conference on Digital Health (ICDH 2023), for <a href="/publication/2023-07-08">"Interpreting County-Level COVID-19 Infections using Transformer and Deep Learning Time Series Models"</a>.</span></li>
  </ul>
</div>

<div class="hp-pub-group">
  <div class="hp-pub-label">Competition Awards</div>
  <ul class="hp-news-list">
    <li class="hp-news-item"><span class="hp-news-date">Jun 2026</span><span class="hp-news-text"><strong>Bronze Medal</strong> (top 10%, 279th of 3677 teams) in <a href="https://www.kaggle.com/competitions/hull-tactical-market-prediction">Hull Tactical Market Prediction</a>, Kaggle.</span></li>
    <li class="hp-news-item"><span class="hp-news-date">Jul 2025</span><span class="hp-news-text"><strong>Silver Medal</strong> (top 5%, 155th of 3757 teams) in <a href="https://www.kaggle.com/competitions/jane-street-real-time-market-data-forecasting">Jane Street Real-Time Market Data Forecasting</a>, Kaggle.</span></li>
  </ul>
</div>

<a class="hp-view-all" href="/awards/">See all awards →</a>
</section>

<script>
(function () {
  var toggle = document.getElementById('hp-news-toggle');
  if (!toggle) return;
  var hidden = document.querySelectorAll('#hp-news-list .hp-news-hidden');
  toggle.addEventListener('click', function () {
    var expanded = toggle.getAttribute('aria-expanded') === 'true';
    for (var i = 0; i < hidden.length; i++) {
      hidden[i].classList.toggle('hp-news-show', !expanded);
    }
    toggle.setAttribute('aria-expanded', String(!expanded));
    toggle.textContent = expanded ? 'Show more' : 'Show less';
  });
})();
</script>
