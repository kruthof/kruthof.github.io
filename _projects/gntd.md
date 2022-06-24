---
layout: distill
title: GNTD
description: German News: Topic Frequency & Sentiment Development
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

**Release Notes:**
- Version 1.0: Topic frequencies & Topic Sentiments for 2004-2021


## Overview

This dataset provides the relative frequency and sentiment of topics covered by 450.000 Handelsblatt articles between 2004 and 2021 within the subsections Finance, Corporation, Politics and Opinions. 

## Methodology

All articles have been translated to english first. Articles have been encoded using Bidirectional Autoencoder using Transformers (Bert). Next, UMAP has been used to reduce dimensionality from 512 to 10. HDBSCAN has been used for clustering. Sentiments are estimated using FinBert. Overall, 76 unique topics have been identified.

## Visualization
Detailed information can be found using the [visualisation app](https://share.streamlit.io/kruthof/gna/main/app.py)!

The figures below provide an overview about the development of topic frequencies and sentiments over time.

![Frequencies over time ](https://raw.githubusercontent.com/kruthof/kruthof.github.io/master/assets/img/gna/frequencies_over_time.png)

![Sentiments over time ](https://raw.githubusercontent.com/kruthof/kruthof.github.io/master/assets/img/gna/Sentiments_over_time.png)

![Frequency-Scales Sentiments over time ](https://raw.githubusercontent.com/kruthof/kruthof.github.io/bc33ea7f04939c9406db82bade80027002f6b5e1/assets/img/gna/Frequency_Sentiments_over_time.png)


## Download
- [Relative Topic-Frequnecies per months](https://raw.githubusercontent.com/kruthof/kruthof.github.io/master/assets/gntd/GNTD_Relative_Frequency.csv)

- [Topic-Sentiments per month](https://raw.githubusercontent.com/kruthof/kruthof.github.io/master/assets/data/gntd/GNTD_Sentiment.csv)

- [Relative Topic-Frequency scaled Sentiments per month](https://raw.githubusercontent.com/kruthof/kruthof.github.io/master/assets/data/gntd/GNTD_Relative_Frequency_Scaled_Sentiment.csv)

## Cite

    ---
    @Manual{,
    title = {GNTD: German News Topics Dataset},
    author = {Garvin Kruthof},
    year = {2022},
    note = {GNTD version 1.0},
    url = {https://kruthof.github.io/projects/gntd/},
     }
    ---