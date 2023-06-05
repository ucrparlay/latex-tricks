---
layout: default
title: Table Columns
parent: Tables
nav_order: 1
permalink: /tables
---

### Columns Format

```
\begin{tabular}{c|l|r}
\end{tabular}
```

The cells can be specified as:

- `c`: center
- `l`: left
- `r`: right
- `p{5cm}`: fixed width, wrap the text automatically. Aligned at top. 
- `m{5cm}` or `b{5cm}` similar to `p`, but vertically aligned in the middle or at the bottom. 
- `*{num}{cols}`: `num` number of columns aligned with `cols`. For example, `\begin{tabular}{*3c}` creates three centered columns

You can also use `|` or `||` between columns to specify the vertical lines.

Insert `@{}` around `clr` to specify the space around each cell. The default value is 4 spaces (`@{    }`). 

Example:

```
\begin{tabular}{@{}c@{}|@{}l@{ }r}
\end{tabular}
```

More generally, you can put anything in `@{}`. It will add this text to every column. 

Example:

```
\begin{tabular}{@{Time: }l@{   Space: }l}
\end{tabular}
```

You can use `>{}` with package `array` to specify the format for each column.

**Example:**

```
\usepackage{array}
\begin{tabular}{>{\bf}cc}
Time & xxx \\
Space&yyy
\end{tabular}
```
This will make the first column bold.


### Change space between columns



