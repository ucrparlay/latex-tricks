---
layout: default
title: Parallel Trees
parent: Data Structure
nav_order: 3
---

{% include labels.html %}

## Parallel Join-based Trees / Functional Trees

**2016 | SPAA**{: .label}[Just Join for Parallel Ordered Sets](https://dl.acm.org/doi/10.1145/2935764.2935768)
{{newline}}Guy E. Blelloch, Daniel Ferizovic, and Yihan Sun 
{{newline}} {{theory}} {{practice}} **#P-tree algorithms**
{{newline}}[Full Version](https://arxiv.org/abs/1602.02120){{linkbtn}}{{space}}
[Code](https://github.com/cmuparlay/PAM){{linkbtn}}

**2018 | PPoPP**{: .label}[PAM: Parallel Augmented Maps](https://dl.acm.org/doi/abs/10.1145/3200691.3178509)
{{newline}}Yihan Sun, Daniel Ferizovic and Guy E. Blelloch
{{newline}} {{theory}} {{practice}} **#The PAM library**
{{newline}}[Full Version](https://arxiv.org/abs/1612.05665){{linkbtn}}{{space}}
[Code](https://github.com/cmuparlay/PAM){{linkbtn}}

**2018 | ESA**{: .label}[Algorithmic Building Blocks for Asymmetric Memories](https://cs.emis.de/LIPIcs/volltexte/2018/9507/pdf/LIPIcs-ESA-2018-44_.pdf)
{{newline}}Yan Gu, Yihan Sun, and Guy E. Blelloch
{{newline}} {{theory}} {{practice}} **#Asymmetric join-based algorithms**
{{newline}}[Full Version](https://arxiv.org/abs/1806.10370){{linkbtn}}{{space}}

**2019 | ALENEX**{: .label}[Parallel Range, Segment and Rectangle Queries with Augmented Maps](https://epubs.siam.org/doi/10.1137/1.9781611975499.13)
{{newline}}Yihan Sun and Guy E. Blelloch
{{newline}} {{theory}} {{practice}} **#Trees for range, segment and rectangle queries**
{{newline}}[Full Version](https://arxiv.org/abs/1803.08621){{linkbtn}}{{space}}
[Code](https://github.com/cmuparlay/PAM){{linkbtn}}

**2019 | PPoPP**{: .label}[Implementing Parallel and Concurrent Tree Structures](https://dl.acm.org/doi/10.1145/3293883.3302576)
{{newline}}Yihan Sun and Guy E. Blelloch
{{newline}} {{practice}} **#Tutorial of PAM**
{{newline}} [Code](https://github.com/cmuparlay/PAM){{linkbtn}}

**2019 | PVLDB**{: .label}[On Supporting Efficient Snapshot Isolation for Hybrid Workloads with Multi-Versioned Indexes](http://www.vldb.org/pvldb/vol13/p211-sun.pdf)
{{newline}}Yihan Sun, Guy E. Blelloch, Wan Shen Lim, and Andrew Pavlo
{{newline}} {{practice}} **#In-memory database using PAM, MVCC, snapshot isolation**
{{newline}}[Code](https://github.com/cmuparlay/PAM){{linkbtn}}

**2019 | SPAA**{: .label}[Multiversion Concurrency with Bounded Delay and Precise Garbage Collection](https://dl.acm.org/doi/10.1145/3323165.3323185)
{{newline}}Naama Ben-David, Guy E. Blelloch, Yihan Sun, and Yuanhao Wei
{{newline}} {{practice}} **#Garbage collection/MVCC for functional trees**
{{newline}}[Full Version](https://arxiv.org/abs/1803.08617){{linkbtn}}{{space}}

**2019 | PLDI**{: .label}[Low-Latency Graph Streaming Using Compressed Purely-Functional Trees](https://dl.acm.org/doi/10.1145/3314221.3314598)
{{newline}} Laxman Dhulipala, Guy Blelloch, and Julian Shun
{{newline}}[Full Version](https://arxiv.org/abs/1904.08380){{linkbtn}}{{space}}
[Code](https://github.com/ldhulipala/aspen){{linkbtn}}

**2022 | PLDI**{: .label}[PaC-trees: Supporting Parallel and Compressed Purely-Functional Collections](https://dl.acm.org/doi/10.1145/3519939.3523733)
{{newline}} Laxman Dhulipala, Guy Blelloch, and Julian Shun
{{newline}}[Code](https://github.com/ParAlg/CPAM){{linkbtn}}


## Other tree-based data structures

**2018 | SPAA**{: .label}[Parallel Write-Efficient Algorithms and Data Structures for Computational Geometry](https://dl.acm.org/doi/10.1145/3210377.3210380)
{{newline}}Guy E. Blelloch, Yan Gu, Julian Shun and Yihan Sun
{{newline}}{{theory}} **#kd-tree, interval tree, priority search tree**
{{newline}}[Full Version](https://arxiv.org/abs/1805.05592){{linkbtn}}

**2022 | SPAA**{: .label}[Parallel Cover Trees and Applications](https://www.cs.ucr.edu/~yihans/papers/2022/SPAA22/covertree.pdf)
{{newline}}Yan Gu, Zachary Napier, Yihan Sun and Letong Wang
{{newline}} {{theory}} **#parallel cover tree with work and span bounds**