---
layout: default
title: Space Tricks
has_children: true
nav_order: 2
permalink: /space
---


A quick example to everything:

```
%% Set page margins:
\usepackage[lmargin=0.75in,rmargin=0.75in,tmargin=.9in,bmargin=.9in]{geometry} 
%% Can also use:
% \setlength\textwidth{7in} 
% \setlength\textheight{10in}
% \usepackage[text={7in,10in},centering]{geometry}
% \usepackage[margin=1.5in]{geometry} 

%% Use compact caption titles
\usepackage[compact]{titlesec}
%% Change more details using the commands \titlespacing{...}{left-margin}{space-before}{space-after}
% \usepackage{titlesec}
% \titlespacing{\section}{0pt}{1em}{1em}
% \titlespacing{\subsection}{0pt}{1em}{1em}
%% runin subsubsection:
% \titleformat{\subsection}[runin]
{\normalfont\normalsize\bfseries}{\thesubsection}{1em}{\underline{#1.}}

%% this is to change the space below tables/figures 
\setlength{\textfloatsep}{0.5em} 
%% this is to change the space above tables/figures 
\setlength{\intextsep}{0.5em} 

%% remove space above/below equations, should be put inside the document (don't know why)
\setlength{\abovedisplayskip}{3pt}
\setlength{\belowdisplayskip}{3pt}
\setlength{\abovedisplayshortskip}{2pt}
\setlength{\belowdisplayshortskip}{2pt}
```
