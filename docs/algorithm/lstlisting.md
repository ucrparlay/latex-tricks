---
layout: default
title: lstlisting
parent: Algorithms
nav_order: 4
---

## **lstlisting for algorithms**

Another way to show code is to use lstlisting. It shows more like "real code". Below is an example for setup the environment. 

```
\usepackage{listings}

%% LISTING ENVIRONMENT (lstlisting)
\newdimen\zzsize
\zzsize=8pt
\newdimen\kwsize
\kwsize=8pt

\newcommand{\basicstyle}{\fontsize{\zzsize}{1\zzsize}\ttfamily}
\newcommand{\keywordstyle}{\fontsize{\kwsize}{1\kwsize}\ttfamily\bf}

\newdimen\zzlstwidth
\settowidth{\zzlstwidth}{\basicstyle~}
\newcommand{\lcm}{}

\lstset{
  aboveskip=-0.5 \baselineskip,
  belowskip=-0.8 \baselineskip,
  xleftmargin=0.5em,
  basewidth=\zzlstwidth,
  basicstyle=\basicstyle,
  columns=fullflexible,
  captionpos=b,
  numbers=left, numberstyle=\small, numbersep=4pt,
  language=C++,
  keywordstyle=\keywordstyle,
  keywords={return,signature,sig,structure,struct,fun,fn,case,type,datatype,let,fn,in,end,functor,alloc,if,then,else,while,with,AND,start,do,parallel,for,parallel_for},
  commentstyle=\rmfamily\slshape,
  morecomment=[l]{\%},
  lineskip={1.5pt},
  columns=fullflexible,
  keepspaces=true,
  mathescape=true,
  escapeinside={@}{@}
}
```

Then to use it, simply use

```
\begin{lstlisting}[frame=lines]
parallel_for (i = 1; i < n; i++) {
  if (a[i] < 0) a[i]++;
  @\textbf{regular LaTeX code}@ // example of escape symbol
  $a_i$ will be directly generated as math mode
}
\end{lstlisting}
```

It uses like `verbatim` but with keywords specified. Use `@...@` to put regular LaTeX code inside (e.g., special format). Math mode `$...$` will be directly generated. `//...` will generate comment in italic. 