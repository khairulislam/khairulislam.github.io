---
layout: single
permalink: /software/
title: "Software"
author_profile: false
---

<div class="hp-page">

<section class="hp-section">

<div class="hp-sw-intro" markdown="1">
Most of my research ships as a PyTorch library rather than a one-off script. [tslens](https://github.com/khairulislam/tslens) is a Captum-compatible interpretability toolkit that attributes any callable mapping `(batch, seq_len, n_features)` to predictions, with no registry to subclass and nothing to reimplement per model: 14 attribution methods, tested against 30+ time series architectures from linear models to LLM-backed foundation models. AstroSpec, AstroGen and AstroLens take the opposite approach where it fits better, putting published astronomy models behind one registry and interface while preserving survey-specific calibration and native instrument grids instead of resampling everything to a common shape.

The work behind them is as much systems as modeling: distributed data-parallel training on SLURM clusters, `torch.compile` and mixed precision for 3D volumes that do not fit on one GPU, inference optimization for serverless deployment, and GitHub Actions pipelines that test and publish the packages.
</div>

<div class="hp-pub-group">
  <div class="hp-pub-label">Stack</div>
  <dl class="hp-stack">
    <dt>Core</dt>
    <dd><span>PyTorch</span><span>PyTorch Lightning</span><span>NumPy</span><span>Pandas</span><span>Scikit-learn</span><span>TensorFlow</span></dd>

    <dt>Models</dt>
    <dd><span>Hugging Face Transformers</span><span>Diffusers</span><span>Accelerate</span><span>timm</span><span>Captum</span></dd>

    <dt>Scale</dt>
    <dd><span>Distributed Training (DDP)</span><span>Multi-GPU</span><span>Mixed Precision</span><span>SLURM / HPC</span><span>Inference Optimization</span></dd>

    <dt>Cloud</dt>
    <dd><span>AWS Lambda</span><span>SageMaker</span><span>S3</span><span>Docker</span><span>Serverless Deployment</span></dd>

    <dt>Engineering</dt>
    <dd><span>Git</span><span>GitHub Actions CI/CD</span><span>Python Packaging (PyPI)</span><span>Experiment Tracking (W&amp;B)</span><span>Technical Documentation</span></dd>

    <dt>Languages</dt>
    <dd><span>Python</span><span>C++</span><span>SQL</span><span>Swift</span><span>Bash</span></dd>
  </dl>
</div>

<div class="hp-pub-group">
  <div class="hp-pub-label">Libraries</div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">tslens <span class="hp-sw-meta"><i class="fas fa-star" aria-hidden="true"></i> 13</span></div>
    <div class="hp-pub-desc">Time series interpretability for PyTorch: 14 attribution methods behind one Captum-compatible interface, tested against 30+ architectures from linear models to LLM-backed foundation models. Published on PyPI with a MkDocs reference site, pytest suite and GitHub Actions release pipeline.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/khairulislam/tslens">GitHub</a>
      <a href="https://pypi.org/project/tslens/">PyPI</a>
      <a href="https://khairulislam.github.io/tslens/">Docs</a>
    </div>
    <div class="hp-tags"><span>PyTorch</span><span>Captum</span><span>Explainable AI</span><span>Time-Series ML</span><span>Public API Design</span><span>pytest</span><span>GitHub Actions CI/CD</span><span>PyPI Packaging</span><span>Technical Documentation</span></div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">AstroSpec</div>
    <div class="hp-pub-desc">Unified spectral library for astronomy, putting seven spectroscopic models behind one PyTorch interface for source classification, redshift estimation, stellar property inference and self-supervised representation learning on native instrument grids.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/khairulislam/AstroSpec">GitHub</a>
    </div>
    <div class="hp-tags"><span>PyTorch</span><span>Astronomical Spectroscopy</span><span>Foundation Models</span><span>Self-Supervised Learning</span><span>Representation Learning</span><span>Transformers</span><span>Distributed Training</span><span>Multi-GPU</span></div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">AstroGen</div>
    <div class="hp-pub-desc">Generative models for astronomical data in 1D, 2D and 3D, covering diffusion models and VAEs for super-resolution, denoising and conditional generation over images, spectra and simulations.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/khairulislam/AstroGen">GitHub</a>
    </div>
    <div class="hp-tags"><span>PyTorch</span><span>Generative AI</span><span>Diffusion Models</span><span>Variational Autoencoders</span><span>Computer Vision</span><span>Hugging Face Diffusers</span><span>3D Deep Learning</span><span>Distributed Training</span></div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">AstroLens</div>
    <div class="hp-pub-desc">Unified library of vision models for astronomy, covering galaxy morphology classification, strong gravitational lensing and multimodal representation learning, with pretrained foundations such as AstroCLIP and AION-1.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/khairulislam/AstroLens">GitHub</a>
    </div>
    <div class="hp-tags"><span>PyTorch</span><span>Computer Vision</span><span>Vision Transformers</span><span>Multimodal Learning</span><span>Transfer Learning</span><span>Pretrained Models</span><span>Distributed Training</span></div>
  </div>
</div>

<div class="hp-pub-group">
  <div class="hp-pub-label">Paper Code</div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">Cosmo3DFlow</div>
    <div class="hp-pub-venue">KDD 2026</div>
    <div class="hp-pub-desc">Wavelet flow matching for reconstructing the early universe from cosmological simulations.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/UVA-MLSys/Cosmo3DFlow">Code</a>
      <a href="/publication/2026-05-17">Paper</a>
    </div>
    <div class="hp-tags"><span>PyTorch</span><span>PyTorch Lightning</span><span>Flow Matching</span><span>Wavelet Transforms</span><span>3D U-Net</span><span>Scientific Machine Learning</span><span>Multi-GPU Training</span><span>SLURM / HPC</span></div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">AI for Astronomy</div>
    <div class="hp-pub-venue">IJHPCA 2025</div>
    <div class="hp-pub-desc">Cloud framework for data-parallel astronomical model inference on AWS serverless infrastructure.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/UVA-MLSys/AI-for-Astronomy">Code</a>
      <a href="/publication/2025-11-11">Paper</a>
    </div>
    <div class="hp-tags"><span>PyTorch</span><span>timm</span><span>Model Deployment</span><span>AWS Lambda</span><span>AWS Step Functions</span><span>Amazon S3</span><span>Docker</span><span>Serverless Computing</span><span>Distributed Inference</span></div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">Timeseries-Explained</div>
    <div class="hp-pub-venue">AAAI 2025 Workshop (AI4TS)</div>
    <div class="hp-pub-desc">Reference implementation of WinTSR, a windowed temporal saliency rescaling method, benchmarked against local interpretation baselines.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/khairulislam/Timeseries-Explained">Code</a>
      <a href="/publication/2024-12-05">Paper</a>
    </div>
    <div class="hp-tags"><span>PyTorch</span><span>Explainable AI</span><span>Time-Series ML</span><span>Model Evaluation</span><span>Benchmarking</span><span>Reproducible Research</span></div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">Financial Time Series <span class="hp-sw-meta"><i class="fas fa-star" aria-hidden="true"></i> 19</span></div>
    <div class="hp-pub-venue">IEEE BigData 2024 Workshop (LLMs for Finance)</div>
    <div class="hp-pub-desc">Benchmarks transformer and LLM-based forecasters (PatchTST, iTransformer, TimesNet, GPT4TS, TimeLLM) on stock, commodity and financial aid data.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/UVA-MLSys/Financial-Time-Series">Code</a>
      <a href="/publication/2024-11-01">Paper</a>
    </div>
    <div class="hp-tags"><span>PyTorch</span><span>Large Language Models</span><span>Fine-Tuning</span><span>Hugging Face Transformers</span><span>Time-Series Forecasting</span><span>Model Evaluation</span><span>Benchmarking</span></div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">COVID-19 Age Groups</div>
    <div class="hp-pub-venue">AAAI 2024 Workshop (AI4TS)</div>
    <div class="hp-pub-desc">Interpreting the impact of population age groups on COVID-19 infections with deep learning time series models.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/UVA-MLSys/COVID-19-age-groups">Code</a>
      <a href="/publication/2024-03-27">Paper</a>
    </div>
    <div class="hp-tags"><span>PyTorch</span><span>Transformers</span><span>Explainable AI</span><span>Time-Series Forecasting</span><span>Public-Health Analytics</span><span>Model Evaluation</span></div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">SA-Timeseries</div>
    <div class="hp-pub-venue">AAAI/SIGAI Doctoral Consortium 2024</div>
    <div class="hp-pub-desc">Sensitivity analysis of temporal dependencies and spatio-temporal patterns in time series models.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/UVA-MLSys/SA-Timeseries">Code</a>
      <a href="/publication/2024-03-23">Paper</a>
    </div>
    <div class="hp-tags"><span>PyTorch</span><span>Sensitivity Analysis</span><span>Explainable AI</span><span>Time-Series Forecasting</span><span>Spatiotemporal Modeling</span><span>Benchmarking</span></div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">GPCE-COVID</div>
    <div class="hp-pub-venue">IEEE ICDH 2023</div>
    <div class="hp-pub-desc">Interpreting county-level COVID-19 infections using transformer and deep learning time series models.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/UVA-MLSys/gpce-covid">Code</a>
      <a href="/publication/2023-07-08">Paper</a>
    </div>
    <div class="hp-tags"><span>PyTorch</span><span>Transformers</span><span>Time-Series Forecasting</span><span>Public-Health Analytics</span><span>Docker</span><span>Reproducible Research</span></div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">MVAM</div>
    <div class="hp-pub-venue">CPS-IoT Week 2023</div>
    <div class="hp-pub-desc">Multi-variant memory attacks on IoT trust computing.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/arupcsedu/MVAM">Code</a>
      <a href="/publication/2023-05-09">Paper</a>
    </div>
    <div class="hp-tags"><span>Cybersecurity</span><span>IoT Security</span><span>Embedded Systems</span><span>Trust Computing</span><span>Memory Security</span></div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">DP on NLP Bias</div>
    <div class="hp-pub-venue">AAAI 2023 Workshop (PPAI) / Data Engineering Bulletin 2024</div>
    <div class="hp-pub-desc">Measuring how differential privacy during fine-tuning affects bias in pretrained language models.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/khairulislam/DP-on-NLP-Bias">Code</a>
      <a href="/publication/2023-02-13">Paper</a>
    </div>
    <div class="hp-tags"><span>PyTorch</span><span>Natural Language Processing</span><span>Hugging Face Transformers</span><span>Fine-Tuning</span><span>Differential Privacy</span><span>Responsible AI</span><span>Bias Evaluation</span><span>Model Evaluation</span></div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">Predict Code Changes</div>
    <div class="hp-pub-venue">Information and Software Technology 2022</div>
    <div class="hp-pub-desc">Early prediction of merged vs abandoned code changes in modern code review.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/khairulislam/Predict-Code-Changes">Code</a>
      <a href="/publication/2022-02-01">Paper</a>
    </div>
    <div class="hp-tags"><span>Python</span><span>Applied ML</span><span>Predictive Modeling</span><span>Feature Engineering</span><span>Classification</span></div>
  </div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">Anomaly Detection on UNSW-NB15 <span class="hp-sw-meta"><i class="fas fa-star" aria-hidden="true"></i> 9</span></div>
    <div class="hp-pub-venue">ITNAC 2020</div>
    <div class="hp-pub-desc">Network traffic anomaly detection with LightGBM and ensemble gradient boosting on the UNSW-NB15 benchmark.</div>
    <div class="hp-pub-links">
      <a href="https://github.com/khairulislam/Anomaly-Detection-on-UNSW-NB15">Code</a>
      <a href="/publication/2020-11-27">Paper</a>
    </div>
    <div class="hp-tags"><span>Python</span><span>LightGBM</span><span>Gradient Boosting</span><span>Anomaly Detection</span><span>Feature Engineering</span><span>Applied ML</span></div>
  </div>
</div>

<div class="hp-pub-group">
  <div class="hp-pub-label">Other Projects</div>

  <div class="hp-pub-item">
    <div class="hp-pub-title">VLASS Vision <span class="hp-sw-meta"><i class="fas fa-star" aria-hidden="true"></i> 5</span></div>
    <div class="hp-pub-desc">Vision models for classifying radio astronomy images from the VLA Sky Survey, comparing CNN and transformer backbones (ResNet, MobileNet, ViT, SwinViT).</div>
    <div class="hp-pub-links">
      <a href="https://github.com/khairulislam/VLASS-Vision">GitHub</a>
    </div>
    <div class="hp-tags"><span>PyTorch</span><span>PyTorch Lightning</span><span>Computer Vision</span><span>timm</span><span>Transfer Learning</span><span>Model Evaluation</span></div>
  </div>
</div>

<a class="hp-view-all" href="https://github.com/khairulislam">See all on GitHub →</a>
</section>

</div>
