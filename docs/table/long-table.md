---
layout: default
title: Long Table
parent: Tables
nav_order: 3
permalink: /tables
---

Using the `longtable` package allows you to insert page breaks between tables. 
[Source](https://www.overleaf.com/learn/latex/Tables)
[Document](https://ctan.math.utah.edu/ctan/tex-archive/macros/latex/required/tools/longtable.pdf)

```
\usepackage{longtable}
```

```
\begin{longtable}[c]{| c | c |}
 \caption{Long table caption.\label{long}}\\

 \hline
 \multicolumn{2}{| c |}{Begin of Table}\\
 \hline
 Something & something else\\
 \hline
 \endfirsthead

 \hline
 \multicolumn{2}{|c|}{Continuation of Table \ref{long}}\\
 \hline
 Something & something else\\
 \hline
 \endhead

 \hline
 \endfoot

 \hline
 \multicolumn{2}{| c |}{End of Table}\\
 \hline\hline
 \endlastfoot

 Lots of lines & like this\\
 \end{longtable}
```

`\endfirsthead`: everthing before this will appear as the first head in the first page

`\endhead`: everything before this after `\endfirsthead` will appear as the first several rows on every page 

`\endfoot`: similarly this defines the foot for every page

`\endlastfoot`: the last line in the table