---
layout: distill
title: GNA
description: German News Analysis
img: 
importance: 1
category: datasets


authors:
  - name: Garvin Kruthof
    url: "https://kruthof.github.io"
    affiliations:
      name: TUM

# Optionally, you can add a table of contents to your post.
# NOTES:
#   - make sure that TOC names match the actual section names
#     for hyperlinks within the post to work correctly.
#   - we may want to automate TOC generation in the future using
#     jekyll-toc plugin (https://github.com/toshimaru/jekyll-toc).
toc:
  - name: Overview
  - name: Methodology
  - name: Visualization
  - name: Download

    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2



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

This project provides an overview about the relative frequency and sentiment of individual topics published in the Handelsblatt between 2004 and 2021 within the subsections Finance, Corporation, Politics and Opinions. 

***

## Methodology

All articles have been translated to english first. Articles have been encoded using Bidirectional Autoencoder using Transformers (Bert). Next, UMAP has been used to reduce dimensionality from 512 to 10. HDBSCAN has been used for clustering. Sentiments are estimated using FinBert. Overall, 76 unique topics have been identified.

## Visualization
soon...

## Download
soon...