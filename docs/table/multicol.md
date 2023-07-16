---
layout: default
title: Multicolumn/Multirow
parent: Tables
nav_order: 4
---

#### Package:

```
\usepackage{multicol,multirow}
```

#### Format:

```
\multicolumn{2}{|c|}{Multiple column}\\
\multirow{3}{4em}{Multiple row}
\multirow{3}{*}{Multiple row} % Use * for default
```



#### Example:
```
\begin{table}[t]
    \centering
\begin{tabular}{ccc}
    \hline
    foo & 10 & 5.6\\
    bar&12&7.0\\\hline
    \multicolumn{2}{c}{abcde} & 12\\\hline
    \multirow{2}{*}{abc} & 4 &4 \\\cline{2-3}
    &2&7\\\hline
    \end{tabular}
    \caption{Multicolumn and Multirow}
\end{table}
```

![table-multicol]({{site.url}}/latex-tricks/img/table/multicol.png)