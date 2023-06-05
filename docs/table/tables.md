---
layout: default
title: Tables
has_children: true
nav_order: 3
permalink: /tables
---

### General Interface

```
\begin{tabular}[pos]{cols}
 table content
\end{tabular}
```

### Text Positions

The `pos` parameter above can be specified as follows:

`t`: aligned top

`b`: aligned bottom

`c` or none (default): aligned middle

### Table Position

```
\begin{table}[table-position]
\end{table}
```

The `table-position` parameter can be:

`h`: approximately here

`t`: top of the page

`b`: bottom of the page

`p`: special table page

`!`: add `!` after the option to override internal parameters

`H`: Exactly here. Similar to `h!`


### Captions

You can use `captionof` to change the caption of a table to a figure, and vice versa. 

```
\captionof{table}{Your caption here} 
```
### Spacing 

Refer to [space/floating](docs/space/floating-equation.html)

