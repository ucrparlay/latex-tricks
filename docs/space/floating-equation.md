---
layout: default
title: Floating and Equation
parent: Space Tricks
nav_order: 3
---

## Floating (figures/tables/algorithm) spacing

A list of spacing settings:

- `abovecaptionskip` and `belowcaptionskip`: space around the caption
- `\floatsep`: Space between multiple floatings
- `\textfloatsep`: space below floating (distance to the rest of text)
- `\intextsep`: space above tables/figures (distance from the text above)
- `\dbltextfloatsep`: for double-column floatings (e.g., `figure*` and `table*`), the distance from the floating to the text
- `\dblfloatsep`: for double-column floatings (e.g., `figure*` and `table*`), the distance between floatings


**Example:**

```
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
```


## Display skip

Change skip above/below equations.

**Example**

```
\setlength{\abovedisplayskip}{3pt}
\setlength{\belowdisplayskip}{3pt}
\setlength{\abovedisplayshortskip}{2pt}
\setlength{\belowdisplayshortskip}{2pt}
```

