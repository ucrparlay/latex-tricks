---
layout: default
title: Enumerate / Item
parent: Space Tricks
nav_order: 4
---

{% include labels.html %}

## Item spacing

**Package** [[documentation]](https://ctan.math.illinois.edu/macros/latex/contrib/enumitem/enumitem.pdf)


```
\usepackage{enumitem}
```

See an illustration here:

![enumitem]({{site.url}}/latex-tricks/img/enumitem.png)

**Vertical spacing settings**

```
\setlength{\topsep}{0pt} % distance from the top to first item
\setlength{\itemsep}{0pt} % distance between two paragraphs in the same item
\setlength{\parsep}{0pt} % distance between two items
```

The distance between the last item to the following text is the same as the one from the text to the first item.

Effectively, the distance between the list and the text is `topsep+parskip` (`parskip` is the spacing between paragraphs in your paper). The distance between two items is `itemsep+\parsep` (both defined above). 


You can remove *all* vertical seperations by using

```
\begin{enumerate}[nosep]
\end{enumerate}
```

You can also use `noitemsep` to kill all space of `itemsep` and `parsep`.

Or you can set this for all lists in your paper by

```
\setlist{nosep}
```

**Horizontal spacing settings**

```
\setlength{\labelwidth}{2em} % the width for the label
\setlength{\labelsep}{2em} % the length from the label to the first word in the item
\setlength{\leftmargin}{2em} % the distance from the left (where text starts) to the left boundary for the item contents; label may go even to the left.
\setlength{\listparindent}{2em} % indent of the paragraph inside each item
```

You can use `wide` to remove indents.

You can also put everything into the list setting:

```
\begin{enumerate}[topsep=0.3em, itemsep=0em, leftmargin=*,wide]
\end{enumerate}
```