---
layout: page
title: refinda
description: A Python Package for Reproducible Financial Data
img: 
importance: 1
category: open source
display_categories: [refinda datasets]

---

The purpose of of this package is to improve `reproducibility of research` at the intersection of machine learning and finance by providing `standardized datasets` and `build-in methods` for data processing and common trading strategies. [Github Repository](https://github.com/kruthof/refinda) `WIP`


## Cite

    ---
    @Manual{,
    title = {Refinda: A Python Package for Reproducible Financial Data},
    author = {Garvin Kruthof},
    year = {2022},
    note = {Refinda 1.0},
    url = {https://kruthof.github.io/projects/reifinda},
     }
    ---

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
