---
layout: default
title: Side caption and wrapfigure
parent: Figures
nav_order: 4
---

## **Side Caption**
Sidecap allows to put the caption on the side [[document]](https://ctan.math.illinois.edu/macros/latex/contrib/sidecap/sidecap.pdf)

```
\usepackage[rightcaption][sidecap]
\begin{SCtable} [relwidth][float] ... \end{SCtable}
\begin{SCfigure} [relwidth][float] ... \end{SCfigure}
\begin{SCtable*} [relwidth][float] ... \end{SCtable*}
\begin{SCfigure*}[relwidth][float] ... \end{SCfigure*}
```

`relwidth` is the relative width to the figure or table. `float` is the regular floating option (e.g., `tbp`).

A more general way to put side caption is to use minipage/tabular to set up the table/figure and the caption separately. You can align the arbitrarily. 

```
\begin{figure}
\begin{tabular}{b{3cm}b{4cm}}
  \centering\includegraphics[width=3cm]{go.png} &
  \caption{A long caption \lipsum[1][1]} \\
\end{tabular}
\caption{sidecaption by tabular.}
\end{figure}
```

![sidcap]({{site.url}}/latex-tricks/img/figure/sidecap.png)

### **Wrapfigure**

Wrapfigure allows for a figure to be wrapped by texts. [[document]](https://mirror.math.princeton.edu/pub/CTAN/macros/latex/contrib/wrapfig/wrapfig-doc.pdf)

```
\usepackage{wrapfig}
\begin{wrapfigure}[lineheight]{position}[overhang]{width}
  ...
\end{wrapfigure}
```

`lineheight` is the number of lines to be packed to fit the wrapfigure. `overhang` is how much the figure should hang out into
the margin. 

Here `[lineheight]` and `[overhang]` can be omitted. 

#### **Example**

```
\begin{wrapfigure}[3]{r}{0.2\columnwidth} %this figure will be on the right wrapped by texts
    \includegraphics[width=\columnwidth]{mesh}
	\caption
\end{wrapfigure}
```

`r` means right. Use `l` for left. 