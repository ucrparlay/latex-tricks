---
layout: default
title: Math
has_children: true
nav_order: 6
---

## **Math**

Use the packages below.

```
%\usepackage{latexsym,amsthm,amsmath,amsfonts,amssymb,stmaryrd,mathtools}
```

Use `$...$` to inline a formula. Use `$$...$$` to write a formula on a single line. The environments `equation` or `align` can also provide formula that are not inline. `equation` is for a single formula. `align` provides multiple lines of formula, aligned by `&` (just like tables). 

Example:

```
\begin{align}
&(a+b)^2-2ab
=&a^2+2ab+b^2-2ab
=&a^2+b^2
\end{align}
```

### 

```
$$
f(x) = 
\begin{cases}
x, & \text{for } x\ge 0 \\
-x, & \text{for } x<0 \\
\end{cases}
$$
```

Or you can also use `left\{` with array for a simular fomula:

```
$$
f(x) = \left\{
\begin{array}{lr}
x, & \text{for } x\ge 0 \\
-x, & \text{for } x<0 \\
\end{array}
$$
```

the `array` or `cases` can also be nested. 

### Define a new "Theorem"

```
\newtheorem{theorem}{Theorem}[section]
\newtheorem{lemma}[theorem]{Lemma}
\newtheorem{corollary}[theorem]{Corollary}
\newtheorem{claim}[theorem]{Claim}
\newtheorem{fact}[theorem]{Fact}
\newtheorem{invariant}[theorem]{Invariant}
\newtheorem{definition}{Definition}
\newtheorem{remark}{Remark}
```

You can also define a different theorem style (i.e., how a theorem is displayed). For example, below we define a more compact version with smaller spaces around. 

```
% compact theorem
\newtheoremstyle{exampstyle}
{.5em} % Space above
{1em} % Space below
{\it} % Body font
{.5em} % Indent amount
{\it \bfseries} % Theorem head font
{.} % Punctuation after theorem head
{.5em} % Space after theorem head
{} % Theorem head spec (can be left empty, meaning `normal')
\theoremstyle{exampstyle} \newtheorem{compactdef}{Definition}
```

Then you can use `\begin{compactdef}..\end{compactdef}` to define a Definition in this style.  

Below is an example for a more compact proof by redefining the `proof` environment. You can change the spaces around. 

```
% compact proof
\makeatletter
\renewenvironment{proof}[1][\proofname]{\par
\vspace{-2\topsep} % remove the space after the theorem
\pushQED{\qed} %
\normalfont
\topsep0pt \partopsep0pt % no space before
\trivlist
\item[\hskip\labelsep
      \itshape
  #1\@addpunct{.}]\ignorespaces
}{
\popQED\endtrivlist\@endpefalse
%\addvspace{3pt plus 3pt} % some space after
}
```