---
layout: default
title: Page Margin
parent: Space Tricks
nav_order: 1
---

## Page Margin:

**Package** [[documentation]](https://mirrors.mit.edu/CTAN/macros/latex/contrib/geometry/geometry.pdf)


```
\usepackage{geometry}
```

Example:

```
\usepackage[lmargin=0.75in,rmargin=0.75in,tmargin=.9in,bmargin=.9in]{geometry}
\setlength\textwidth{7in} 
\setlength\textheight{10in}
\usepackage[text={7in,10in},centering]{geometry}
\usepackage[margin=1.5in]{geometry} 
```

If `\usepackage{geometry}` is already used, you can set the parameters using:

```
\geometry{lmargin=1in,rmargin=1in,tmargin=1in,bmargin=1in}
```

Change other global settings for spacing:

```
\setlength{\parindent}{0em}  % Changes the indent of paragraph
\setlength{\parskip}{0em} % Changes the spacing between paragraphs
\addtolength{\parskip}{0.15ex} % add 0.15ex to parskip
\renewcommand{\baselinestretch}{.97} % Changes spacing between lines
```