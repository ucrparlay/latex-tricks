---
layout: default
title: Spacing
parent: Algorithms
nav_order: 2
---

## **Adjust spacing for Algorithms**

The following code removes the right hand margin in an algorithm:

```
\makeatletter
% Remove right hand margin in algorithm
\patchcmd{\@algocf@start}% <cmd>
  {-1.5em}% <search>
  {0pt}% <replace>
  {}{}% <success><failure>
```

The following code adjust the left margin:

```
\setlength{\algomargin}{.5em}   % left margin
```

For general spacing around algorithm, it is the same as regular floating. See details here: [space/floating](/latex-tricks/docs/space/floating-equation.html)
