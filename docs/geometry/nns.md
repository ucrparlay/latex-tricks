---
layout: default
title: Nearest Neighbor
parent: Geometry
nav_order: 3
---
{% include labels.html %}

# **Nearest Neighbor Search (NNS)**

## **Exact Nearest Neighbor Search (NNS)**

### Cover Tree

**2006 | ICML**{: .label}[Cover trees for nearest neighbor](https://dl.acm.org/doi/10.1145/1143844.1143857)
{{newline}}Alina Beygelzimer, Sham Kakade, and John Langford
{{newline}} {{sequntial}} {{theory}} {{practice}} **#original cover tree paper**
{{newline}}[Full Version](https://hunch.net/~jl/projects/cover_tree/paper/paper.pdf){{linkbtn}}{{space}}
[Project Page](https://hunch.net/~jl/projects/cover_tree/cover_tree.html){{linkbtn}}

**2006 | Tech Report**{: .label}[Fast Nearest Neighbors](http://tkollar.s3.amazonaws.com/papers/other/fastNN2006.pdf)
{{newline}}Thomas Kollar
{{newline}} {{sequential}} {{theory}} **#correction for the cover tree paper**

**2015 | thesis**{: .label}[Improving Dual-tree Algorithms](https://smartech.gatech.edu/bitstream/handle/1853/54354/CURTIN-DISSERTATION-2015.pdf)
{{newline}} {{sequential}} {{theory}} {{practice}} **#Ryan R. Curtin's Ph.D. thesis, correction for the cover tree paper, &nbsp;&nbsp;&nbsp;&nbsp;experimental study of cover trees**

**2015 | ICML**{: .label}[Faster Cover Trees](https://proceedings.mlr.press/v37/izbicki15.html)
{{newline}}Mike Izbicki and Christian R. Shelton
{{newline}} {{practice}} **#parallel implementation (but relaxing cover tree invariants)**

**2017 | thesis**{: .label}[Divide and Conquer Algorithms for Machine Learning](https://izbicki.me/public/papers/dissertation.pdf)
{{newline}}Mike Izbicki 
{{newline}} {{practice}} **#Mike Izbicki's Ph.D. thesis**

**2021 | preprint**{: .label}[A new compressed cover tree guarantees a near linear parameterized complexity for all k-nearest neighbors search in metric spaces](https://arxiv.org/pdf/2111.15478.pdf)
{{newline}}Yury Elkin and Vitaliy Kurlin
{{newline}} {{theory}} **#correction for the cover tree paper, compressed version**

**2022 | SPAA**{: .label}[Parallel Cover Trees and Applications](https://www.cs.ucr.edu/~yihans/papers/2022/SPAA22/covertree.pdf)
{{newline}}Yan Gu, Zachary Napier, Yihan Sun and Letong Wang
{{newline}} {{theory}} **#parallel cover tree with work and span bounds**

### Others

**2002 | STOC**{: .label}[Finding Nearest Neighbors in Growth-restricted Metrics](https://dl.acm.org/doi/10.1145/509907.510013)
{{newline}}David R. Karger and Matthias Ruhl
{{newline}} {{theory}} **#Metric Skip List, defined expansion rate/KR dimension**

## Approximate Nearest Neighbor Search (ANNS)

### Graph-based

### LSH-based

