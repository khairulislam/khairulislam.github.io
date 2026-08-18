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

* Python (PyTorch, TensorFlow, Scikit-learn)
* C++
* Web: HTML, JavaScript, Markdown

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
