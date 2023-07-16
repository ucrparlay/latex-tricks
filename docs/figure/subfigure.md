---
layout: default
title: Subcaption and subfigures
parent: Figures
nav_order: 4
---

## **Subcaption / subfigures**
Use the packages below ([document](https://ctan.math.utah.edu/ctan/tex-archive/macros/latex/contrib/caption/subcaption.pdf)):

```
\usepackage{subcaption}
```

You can also add options as:

```
\usepackage[labelfont=bf,list=true,skip=0em]{subcaption}
```

`skip` means the vertical space before subcaption. 

You can also adjust the setting by:

```
\subcaptionsetup[figure]{skip=0em}
\captionsetup[figure]{skip=0em}
```

#### **Example:**

The following generate a figure with two subfigures, each with a subcaption.

```
\begin{figure}
\centering
\subcaptionbox{A cat\label{cat}}[0.4\columnwidth]
{\includegraphics{cat}}
\subcaptionbox{A dog\label{dog}}[0.5\columnwidth]
{\includegraphics{dog}}
\caption{Two animals}\label{animals}
\end{figure}
```

The following generate two side-by-side figures, each with a caption.
```
\begin{figure}
\centering
\captionbox{A cat\label{cat}}
[.4\textwidth]{\includegraphics{cat}}%
\captionbox{A dog\label{dog}}
[.4\textwidth]{\includegraphics{dog}}
\end{figure}
```

You can use `\subref{cat}` to refer to the subfigure label without figure label (e.g., Figure a). Otherwise it will give you the figure + subfigure label (e.g., Figure 7a). 


### **Subscaptiongroup**
A better and probably more general way is to use `subcaptiongroup`. It will label all labels inside this environment as subcaptions. Then you can just use any way inside the environment to align the figures and captions. The following example aligns pictures with different sizes and 

```
\begin{table}
\begin{subcaptiongroup}
\begin{tabular}{p{3cm}p{4cm}}
  \centering\includegraphics[width=1cm]{go.png} &
  \includegraphics[width=3cm]{go.png} \\ 
  \caption{caption 1} & \caption{Caption 2. It can be very very very very very very long, which takes multiple lines.}
\end{tabular}
\end{subcaptiongroup}
\caption{subfigures}
\end{table}
```

You can also make each caption a subcaptionbox to get the same result. 

```
\begin{figure}
\begin{tabular}{p{3cm}p{4cm}}
  \centering\includegraphics[width=1cm]{go.png} &
  \includegraphics[width=3cm]{go.png} \\
  \subcaptionbox{caption 1}[3cm]{} & \subcaptionbox{Caption 2. It can be very very very very very very long, which takes multiple lines.}[4cm]{}\\
  \hline
\end{tabular}
\caption{subfigures}
\end{figure}
```

Both will give you the same figure below:

![subfig]({{site.url}}/latex-tricks/img/figure/subfigure.png)

But `subcaptiongroup` seems to generate larger space below subcaption. 

### **Subcaption settings**

You can change the setup for subfigure/subtable as:

```
% This only changes the setting for subtable, instead of table.
\captionsetup[table]{textfont=bf,position=bottom}
\captionsetup[figure]{textfont=bf,position=bottom}
```

### **More about captions**

See [captions]({{site.url}}/docs/caption/caption.html)