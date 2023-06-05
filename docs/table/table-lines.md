---
layout: default
title: Horizontal Lines
parent: Tables
nav_order: 2
permalink: /tablelines
---

You can use `hline` for a thinner line that takes little additional space. Similarly use `\cline{x-y}` to make this line to cover only column x to y. 

With package `booktabs`, you can also use `bottomrule`, `toprule` and `midrule` to make the lines wider and nicer. Similarly, `cmidrule` can be used to make a partial `midrule`. The syntax is:

```
\cmidrule[thickness](shortening){colstart-colend}
```

Package:

```
\usepackage{booktabs}
```

Example ([Source](https://tex.stackexchange.com/questions/116474/midrule-that-extends-only-over-some-of-the-columns-in-booktabs)):

```
\cmidrule(lr{1em}){2-3}
\cmidrule[2pt](lr){1-1}
```

For `toprule` and `bottomrule` you can also specify the thickness in a similar way:

```
\toprule[5pt]
```

