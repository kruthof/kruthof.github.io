---
layout: distill
title: French49
description: French 49 Industry Portfolio + Technical Indicators
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
  - name: Features

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

The dataset is based on the [49 industry portfolios data](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/Data_Library/det_49_ind_port.html) published by Kenneth R. French using equally weighting method. The original data features missing values until mid 1969. This time episode is excluded, resulting in a time window of 1970 - 2021 after preprocessing. Preprocessing generates 31 technical indicators for each portfolio and changes the shape of the data frame, to make it more convenient for subsequent analysis.

***

## Features

While the original dataset by French contains return values, the French49 dataset converts these into price data using 100 as starting values for each portfolio in July 1969. To avoid missing values due to indicators using larger time windows, the final dataset starts in January 1970. Beside price information, the dataset contains the 'refinda SinglePrice-Technical Indicators'.  
<div id="body">
  
</div>
<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script  src="./script.js"></script>

<div style="display: none">
    <![CDATA[<script src="http://d3js.org/d3.v3.min.js" charset="utf-8">
    <!--<![CDATA[--><![CDATA[
    </script>
    <![CDATA[<script src="./script.js">
    <!--<![CDATA[--><![CDATA[
    // <![CDATA[
    </script><![CDATA[]]>
</div>
