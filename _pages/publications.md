---
layout: page
permalink: /publications/
title: Publications
description: Selected publications and working papers.
years: [2026, 2025, 2023]
nav: true
---


<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
