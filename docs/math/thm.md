---
layout: default
title: New keywords
parent: Algorithms
nav_order: 2
---

## **Define new keywords in algorithms**

### **Input/output keywords**

`\SetKwInOut{notes}{Notes}` or `\SetKwInput{notes}{Notes}` can define a new keyword `Note` with command as `\note{...}`. The difference between `InOut` and `Input` is that `InOut` aligns the position of `:` for all input/output entries. For space saving, `SetKwInput` is always better. The document also specified multiple ways to align the position of `:` for multiple keywords. 

By default, the description of the keyword will be put in a box after the keyword (i.e., all following lines will have a large indent). A adhoc way to fix this is to use `pushline` and `popline`.

```
\newcommand{\nosemic}{\renewcommand{\@endalgocfline}{\relax}}% Drop semi-colon ;
\newcommand{\dosemic}{\renewcommand{\@endalgocfline}{\algocf@endline}}% Reinstate semi-colon ;
\newcommand{\popline}{\Indm\dosemic}% Undent
\newcommand{\pushline}{\Indp}% Indent
```

#### Example:

```
% \notations uses the default setting
\notations{a  very very very long description. It will have an indent aligned to the title of this entry.\\Adding a new line will start from the very left.} 
% \maintains is adjusted by pushline
\maintains{ A long sentence with less indent to the left. \\ \pushline When adding a new line it has a small indent. All following sentences follow the same indent. \lipsum[1][2]}
```

![pushline]({{site.url}}/latex-tricks/img/algorithm/pushline.png)

### **New "for" keyword**

```
\SetKwFor{parForEach}{ParallelForEach}{do}{endfor}
```

Then you can use `\parForEach` as a regular `\For` command. It can also be prefixed with `l` (i.e., `\lparForEach`) to make it one line. 

### **New "function" keyword**

Define a function as:

```
\SetKwProg{myfunc}{Function}{}{}
```

Then we can use `\myfunc{function name}{content}` to define a function.

