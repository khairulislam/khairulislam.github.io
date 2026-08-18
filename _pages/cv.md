---
layout: archive
title: "CV"
permalink: /cv/
redirect_from:
  - /resume
---

{% include base_path %}

## Education

* Ph.D. in Computer Science, [University of Virginia](https://engineering.virginia.edu/department/computer-science), (2021 – Present)
* M.E. in Computer Science, [University of Virginia](https://engineering.virginia.edu/department/computer-science), 2024
* B.Sc. in Computer Science and Engineering, [Bangladesh University of Engineering and Technology](https://cse.buet.ac.bd/), 2018

## Work Experience

* Spring 2021 – Present: Graduate Research Assistant
  * Computer Science, University of Virginia
  * Duties: Time series deep learning and interpretation
  * Supervisor: Professor Judy Fox

* Dec 2018 – Dec 2020: Software Developer
  * Samsung Research, Dhaka, Bangladesh
  * Duties: iOS app development
  * Skills: Swift, C++, Agile development

* Summer 2018: Research Intern
  * REVE Systems Limited, Dhaka, Bangladesh
  * Duties: Bengali speech recognition and data collection
  * Skills: PyTorch

## Skills

* **Deep learning**: transformers, diffusion and flow matching models, foundation models and self-supervised pretraining, LLM fine-tuning and prompting, sequence and time series modeling, explainable AI and feature attribution
* **Frameworks and libraries**: PyTorch, Hugging Face (Transformers, Diffusers, Accelerate), TensorFlow, Scikit-learn, NumPy, Pandas, Captum, Weights & Biases
* **Training and inference at scale**: multi-GPU and distributed training (DDP), mixed precision, HPC clusters (SLURM), model optimization for inference, serverless deployment on AWS Lambda, Docker
* **Cloud and data**: AWS (SageMaker, S3, Lambda), large-scale data pipelines, experiment tracking and reproducible training workflows
* **Programming languages**: Python, C++, SQL, Swift, JavaScript, Bash
* **Software engineering**: Git, GitHub Actions CI/CD, Django, PostgreSQL, REST APIs, agile development, open-source library development ([tslens](https://github.com/khairulislam/tslens) on PyPI)
* **Communication**: 7+ peer-reviewed publications, conference talks, teaching assistant for seven graduate and undergraduate courses

## Publications

<ul>{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

<!-- Talks
<ul>{% for post in site.talks reversed %}
  {% include archive-single-talk-cv.html %}
{% endfor %}</ul> -->

## Teaching

<ul>{% for post in site.teaching reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>
