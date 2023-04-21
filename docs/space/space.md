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
% {\normalfont\normalsize\bfseries}{\thesubsection}{1em}{}
%% Set special format for title: 
% \newcommand{\mysubsection}[1]{\underline{#1}.}
% \titleformat{\subsection}[runin]
% {\normalfont\normalsize\bfseries}{\thesubsection}{1em}{\mysubsection}

% Space around the caption
\setlength\abovecaptionskip{0em}
\setlength\belowcaptionskip{0.3em}
% Space between multiple floatings
\setlength{\floatsep}{0em}
% space below floating (distance to the rest of text)
\setlength{\textfloatsep}{0.5em}
% space above tables/figures (distance from the text above)
\setlength{\intextsep}{0.5em} 
%%%%% these two are for double-column floatings, e.g., figure* and table*
\setlength{\dbltextfloatsep}{1em} % floating to text
\setlength{\dblfloatsep}{0.5em} % between floatings

%% remove space above/below equations, should be put inside the document (don't know why)
\setlength{\abovedisplayskip}{3pt}
\setlength{\belowdisplayskip}{3pt}
\setlength{\abovedisplayshortskip}{2pt}
\setlength{\belowdisplayshortskip}{2pt}
```

For space around tables/figures/algorithms, refer to [floating](docs/space/floating-equation.html)