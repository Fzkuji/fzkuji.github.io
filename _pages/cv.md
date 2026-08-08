---
layout: archive
title: ""
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D in Data Science, City University of Hong Kong, 2023 - Present
* M.S. in Advanced Computer Science, University of Sheffield, 2021 - 2022
* B.Eng in Software Engineering, Xi'an Jiaotong University, 2017 - 2021

Work experience
======
* August 2024 - Present: Researcher
  * Tencent Jarvis Research Center
  * Duties includes: Develop model merging methods for multi-task learning and knowledge editing
  * Supervisor: Dr. Xian Wu, Prof. Yefeng Zheng

* July 2023 - April 2024: Researcher
  * Huawei Noah's Ark Lab
  * Duties included: Leverage LLMs for multi-domain CTR prediction
  * Supervisor: Li Xiangyang

  
Skills
======
* Programming Languages and Technologies
  * Proficient in Java, Python, and C
  * Web Development: Java EE, WeChat Mini Program, JavaScript
* Machine Learning and AI
  * PyTorch and deep learning frameworks
  * Large Language Models (LLMs)
  * Natural Language Processing
  * Computer Vision
  * Transformers and PEFT libraries
* Project Management and Leadership
  * Full development cycle experience
  * Team Leadership & Organization
  * Requirements analysis and design
  * Student Union management experience


Publications
======
{% for category in site.publication_category %}
  {% assign posts = site.publications | where: "category", category[0] | sort: "date" | reverse %}
  {% if posts.size > 0 %}
<h3 class="cv-subhead">{{ category[1].title }}</h3>
<ul class="cv-list">
  {% for post in posts %}
    {% include archive-single-cv.html number=forloop.index %}
  {% endfor %}
</ul>
  {% endif %}
{% endfor %}

Mentorship
======
<ul class="cv-list">{% for post in site.teaching reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

Service
======
* Conference Reviewer: AAAI, KDD, ICDM, NeurIPS, WWW, RecSys, ACMMM
* Journal Reviewer: TKDE, TKDD

Awards and honors
======
* Second Prize, Beijing College Students "Super Individual" (OPC) Entrepreneurship Competition, 2026 — team member. Organised by the Beijing Municipal Education Commission and the Beijing College Students Employment and Entrepreneurship Guidance Center.
* Led a master's student research team to the MSDS Outstanding Performance Award, City University of Hong Kong, 2026
* Tencent Rhino-Bird Outstanding Project, 2023 — ranked 4th out of 26
* Outstanding Dissertation (Top 10%), University of Sheffield, 2022
* First-Class Honours, University of Sheffield, 2022
* Excellent Award, "Tengfei Cup" Innovation and Entrepreneurship Competition, 2019
* Wang Shishao Scholarship, Xi'an Jiaotong University, 2020
* Second Prize, Mathematical Contest in Modeling, 2018
* Third-class Scholarship, Xi'an Jiaotong University, 2018
* Outstanding Student Cadre, Xi'an Jiaotong University, 2018
