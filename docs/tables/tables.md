---
layout: default
title: Tables
has_children: true
nav_order: 3
permalink: /tables
---

### General Interface

```
\begin{tabular}{c|l|r}
\end{tabular}
```

The cells can be specified as:

- `c`: center
- `l`: left
- `r`: right
- `p{5cm}`: fixed width, wrap the text automatically

Insert `@{}` around `clr` to specify the space around each cell. The default value is 4 spaces (`@{    }`). 

Example:

```
\begin{tabular}{@{}c@{}|@{}l@{ }r}
\end{tabular}
```

### Lines Between Rows

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

### Spacing 

Refer to [floating](docs/space/floating-equation.html)