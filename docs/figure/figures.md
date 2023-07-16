---
layout: default
title: Figures
has_children: true
nav_order: 4
---

### General Interface

```
\usepackage{graphicx}
\begin{figure}[pos]
 figure content
 % for inserting an image (need package graphicx)
 \includegraphics[options]{a.pdf} % can also be image extensions e.g., png, jpg
\end{figure}
```

[graphicx document](https://ctan.math.washington.edu/tex-archive/macros/latex/required/graphics/grfguide.pdf)  [Example documents](https://www.overleaf.com/learn/latex/Inserting_Images)

### Figure Positions

The `pos` parameter above can be specified as follows [source](https://www.overleaf.com/learn/latex/Inserting_Images).

`h`: approximately here

`t`: top of the page

`b`: bottom of the page

`p`: special table page

`!`: add `!` after the option to override internal parameters

`H`: Exactly here. Similar to `h!`

### Set the default directory for graphix

This path can be absolute or relative. Then includegraphics will use the folder as the path by default. 

```
%Path relative to the .tex file containing the \includegraphics command
\graphicspath{ {images/} }
%Path relative to the main .tex file 
\graphicspath{ {./images/} }

%Absolute Path in Windows format:
\graphicspath{ {c:/user/images/} }
%Absolute Path in Unix-like (Linux, Mac OS) format
\graphicspath{ {/home/user/images/} }
```

You can also specify more than one paths:

```
\graphicspath{ {./images1/}{./images2/} }
```

### Options

For size:

```
% Specify width, height will be adjusted accordingly
\includegraphics[width=\textwidth]{img}
% Specify width and height, will be enforced to be the size
\includegraphics[width=5cm, height=4cm]{img}
% Specify scale, relative to original size
\includegraphics[scale=1.2]{img}
% Specify angle (e.g., rotate 45 degrees)
\includegraphics[angle=45]{img}
```

For pdf format, you can also specify the page:
```
% only put page 2 of a.pdf as an image
\includegraphics[width=\textwidth, page=2]{a.pdf}
```

### Captions

You can use `captionof` to change the caption of a table to a figure, and vice versa. 

```
\captionof{table}{Your caption here} 
```

You can change the caption of a "table" to be anything by:

```
\renewcommand{\figurename}{Special Figure}
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


### Spacing 

Refer to [space/floating](/latex-tricks/docs/space/floating-equation.html)
