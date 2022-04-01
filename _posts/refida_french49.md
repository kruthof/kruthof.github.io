---
layout: distill
title: French49 Dataset
permalink: /projects/refida/french49/
description: Dataset based on French 49 Portfolio data incl. technical indicators
date: 2022-01
category: open source


authors:
  - name: Garvin Kruthof
    url: "https://kruthof.github.io"
    affiliations:
      name: TUM


bibliography: 2018-12-22-distill.bib

# Optionally, you can add a table of contents to your post.
# NOTES:
#   - make sure that TOC names match the actual section names
#     for hyperlinks within the post to work correctly.
#   - we may want to automate TOC generation in the future using
#     jekyll-toc plugin (https://github.com/toshimaru/jekyll-toc).
toc:
  - name: Overview
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
  - name: Features
  - name: Data Processing
  - name: Usage


# Below is an example of injecting additional post-specific styles.
# If you use this post as a template, delete this _styles block.
_styles: >
  .fake-img {
    background: #bbb;
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: 0 0px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 12px;
  }
  .fake-img p {
    font-family: monospace;
    color: white;
    text-align: left;
    margin: 12px 0;
    text-align: center;
    font-size: 16px;
  }

---

**NOTE:**
WIP


## Overview

The dataset is based on the [49 industry portfolios data](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/Data_Library/det_49_ind_port.html) published by Kenneth R. French using equally weighting method. The original data features missing values until around 1969. This time episode is excluded, resulting in a time window between 1969 - 2021. Preprocessing generates various technical indicators for each portfolio and changes the shape of the data frame, to make it more confinient for subsequent modeling tasks.

***