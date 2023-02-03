---
layout: page
title: ClimateAttention
description: ClimateAttention Classifier
img: 
importance: 1
category: machine learning models

---


# Description:

climateattention-ctw `classifies` if a given sequence is related to `climate topics`. 
Fine-tuned classifier using the balanced ClimaText Wiki-doc corpus, with 115847 samples (57922 positives, 57925 negatives)(Varini et al., 2020) and climatebert/distilroberta-base-climate-f pre-trained model. (Webersinke et al., 2021)


# How to use:
```python
    from transformers import AutoTokenizer, pipeline,RobertaForSequenceClassification
    tokenizer = AutoTokenizer.from_pretrained("climatebert/distilroberta-base-climate-f")
    climateattention = RobertaForSequenceClassification.from_pretrained('kruthof/climateattention-ctw',num_labels=2)
    ClimateAttention = pipeline("text-classification", model=climateattention, tokenizer=tokenizer)
    ClimateAttention('Emissions have increased during the last several months')
    >> [{'label': 'Yes', 'score': 0.9993829727172852}]
```
 # Performance:

Performance tested on the balanced ClimaText Wiki-doc test set, featuring 3826 samples (1913 positives, 1913 negatives) (TSV, 613 KB)(Varini et al., 2020)

|Accuracy|  Precision | Recall  |   F1   |  
|----|-----|-----|-----|
| 0.8834   |  0.8717    |  0.8991 | 0.8852 |  


# Cite:
    ---
    @misc{kruthof2023,
        title={ClimateAttention: A Fine-Tuned Climate Attention Classifier},
        author={Kruthof, Garvin},
        url={https://huggingface.co/kruthof/climateattention-ctw},
        year={2023}
    ---

# References:

Varini, F. S., Boyd-Graber, J., Ciaramita, M., & Leippold, M. (2020). 
ClimaText: A dataset for climate change topic detection. arXiv preprint arXiv:2012.00483.

Webersinke, N., Kraus, M., Bingler, J. A., & Leippold, M. (2021). 
Climatebert: A pretrained language model for climate-related text. arXiv preprint arXiv:2110.12010.


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
