---
layout: default
title: Tables
has_children: true
nav_order: 3
---

### **General Interface for table:**

```
\begin{table}[table-position]
\end{table}
```

The `table-position` parameter can be:

`h`: approximately here

`t`: top of the page

`b`: bottom of the page

`p`: special table page

`!`: add `!` after the option to override internal parameters

`H`: Exactly here. Similar to `h!`


### **Captions**

You can use `captionof` to change the caption of a table to a figure, and vice versa. 

```
\captionof{table}{Your caption here} 
```

You can change the caption of a "table" to be anything by:

```
\renewcommand{\tablename}{Special Table}
```

If you add a table below, it will be shown as `Special Table 1` in caption. 

You can use the `caption` package to change caption format. For example:

```
\usepackage[labelfont=bf,font={small}]{caption}
\usepackage[labelfont=bf,small,aboveskip=2pt,belowskip=2pt]{caption}
```

You can also reset figure or table name globally in the `caption` package.

```
\usepackage[figurename=Fig.,tablename=Tab.]{caption}
```

### **Labels**

It's recommended to put `\label` **inside** the caption. This is especially useful when you have multiple tabular (and thus captions) inside one environment. 

### **General Interface for tabular:**

```
\begin{tabular}[textpos]{cols}
 table content
\end{tabular}
```

`tabular` does not need to be inside a `table` environment. It can be directly put in text (so it won't be a floating). It can also be put in other environments such as figure, algorithm, etc. 

### **Text Positions**

The `textpos` parameter above is for vertical alignment. It can be specified as follows:

`t`: aligned top

`b`: aligned bottom

`c` or none (default): aligned middle

### **Column Options**

The `col` option is explained in [table/table-columns](/latex-tricks/docs/table/columns.html)

### **Subtable**

You can insert subtables in one table environment. They will get two subcaptions. 

#### Example

```
\begin{table}[h]
\begin{subtable}[b]{0.45\textwidth}
  \begin{tabular}{lll}
  A & B & C \\ \hline
  1 & 3 & 5\\
  2 & 4 & 6\\	\hline
  \end{tabular}
  \caption{Subtable 1}\label{tab:subtab1}
\end{subtable}
\hfill
\begin{subtable}[b]{0.45\textwidth}
  \begin{tabular}{lll}
  A & B & C \\ \hline
  1 & 3 & 5\\
  2 & 4 & 6\\	\hline
  \end{tabular}
  \caption{Subtable 2}\label{tab:subtab2}
\end{subtable}
\end{table}
```

![subtable]({{site.url}}/latex-tricks/img/table/subtables.png)

They will be referred to as Table 7a and Table 7b.

By default they are aligned in the middle vertically. You can use `b` to make them align bottom. When they have different heights, this may look better. 

### **Spacing**

Refer to [space/floating](/latex-tricks/docs/space/floating-equation.html)

### **Useful settings**

```
\usepackage{array}% for extended column definitions
% Multi-line column with fixed length. Use \par for a new line.
\newcolumntype{L}[1]{>{\raggedright\let\newline\\\arraybackslash\hspace{0pt}}m{#1}}
\newcolumntype{C}[1]{>{\centering\let\newline\\\arraybackslash\hspace{0pt}}m{#1}}
\newcolumntype{R}[1]{>{\raggedleft\let\newline\\\arraybackslash\hspace{0pt}}m{#1}}
\usepackage{booktabs} % provides toprule, bottomrule, midrule, cmidrule, etc.
\usepackage{multicol,multirow}
\usepackage{longtable} % provides long table
\usepackage{supertabular} % similar to long table, allowing tables to take more than one page
\usepackage{colortbl}
\usepackage{bigstrut}
```