---
layout: default
title: Title Spacing
parent: Space Tricks
nav_order: 2
---

## Title Spacing

**Package** [[documentation]](https://mirror.mwt.me/ctan/macros/latex/contrib/titlesec/titlesec.pdf)

```
\usepackage{titlesec}
```

You can directly use 
```
\usepackage[compact]{titlesec}
```
which provides you a bundle of choices to make section titles more space-efficient. 

**Example**

```
\titlespacing{\section}{ %% 
  0pt}{ %% left margin
  10pt plus 2pt minus 2pt}{ %% space before
  5pt plus 2pt} %% space after
\titlespacing{\paragraph}{ %%
  0pt}{ %%              left margin
  0.3\baselineskip}{ %% space before (vertical)
  1em} %%               space after (horizontal)
```

Using a runin title (in the same line with text):
```
\titleformat{\subsection}[runin]
{\normalfont\normalsize\bfseries}{\thesubsection}{1em}{}
```

Use special format for the title:

```
\newcommand{\mysubsection}[1]{\underline{#1}.}
\titleformat{\subsection}[runin]
{\normalfont\normalsize\bfseries}{\thesubsection}{1em}{\mysubsection}
```
