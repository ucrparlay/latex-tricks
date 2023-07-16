---
layout: default
title: Table Columns
parent: Tables
nav_order: 1
---

## **Columns Format**

```
\begin{tabular}{c|l|r}
\end{tabular}
```

The cells can be specified as:

- `c`: center
- `l`: left
- `r`: right
- `p{5cm}`: fixed width, wrap the text automatically. Aligned at top. 
- `m{5cm}` or `b{5cm}` similar to `p`, but vertically aligned in the middle or at the bottom. 
- `*{num}{cols}`: `num` number of columns aligned with `cols`. For example, `\begin{tabular}{*3c}` creates three centered columns

You can also use `|` or `||` between columns to specify the vertical lines.

#### Example:

```
\begin{tabular}{@{}c@{}|@{}l@{ }r}
\end{tabular}

\begin{tabular}{*3c} % equivalent to ccc
\end{tabular}
```

### ***Fixed width columns with any alignment***

You can also define new column styles:

```
\usepackage{array}% for extended column definitions
\newcolumntype{L}[1]{>{\raggedright\let\newline\\\arraybackslash\hspace{0pt}}m{#1}}
\newcolumntype{C}[1]{>{\centering\let\newline\\\arraybackslash\hspace{0pt}}m{#1}}
\newcolumntype{R}[1]{>{\raggedleft\let\newline\\\arraybackslash\hspace{0pt}}m{#1}}
```

Here `L`, `C` and `R` are left, center and right alignment of a fixed width, e.g., `R{5cm}`. In such fixed-width columns, you can also choose to insert a newline by `par` or `\\`.

```
\begin{tabular}{*3{C{3cm}}L{5cm}}
\end{tabular}
```

### **Self-defined style**

Similarly you can define any style for cell alignment, and use it like `clr`.

```
\usepackage{array}% for extended column definitions
\newcolumntype{B}{>\bf}c}
\begin{tabular}{Bclr}
\end{tabular}
```

### **Special algin one cell**

Use the command below to adjust one cell alignment specially.

```
\newcommand{\minitab}[2]{\multicolumn{1}{#1}{#2}}
```

Then you can put this in any cell to change alignment:

```
\begin{tabular}{|c|c|}
  \hline
  abcdefg& abcdefg \\
  hijkl& mn\\
  \minitab{|l|}{op}& qrst\\
  uvw&xyz\\
  \hline
\end{tabular}
\caption{all are centered except for one cell}
```

![table-multicol]({{site.url}}/latex-tricks/img/table/specialcell.png)

### **Add prefix or suffix for an entire column**

You can use `>{}` or `<{}` with package `array` to specify the format for each column. `>{}` means to insert something at the begining of a cell for an entire column. `<{}` is to insert to the end.

#### Example:

The following example will make the first column bold, and add "time .. s" to the first column and "space .. GB" to the second column.
```
% Example 2:
\begin{table}[t]
    \centering
\begin{tabular}{>{\bf}c >{time:~}c<{s} >{Space:~}c<{~GB}}
    \hline
    foo & 10 & 5.6\\
    bar&12&7.0\\\hline
    \multicolumn{2}{c}{abcde} & 2.0\\\hline
    \multirow{2}{*}{abc} & 4.2 &3.1 \\\cline{2-3}
    &5.4&6.3\\\hline
    \end{tabular}
    \caption{Add ``time .. s'' to the first column and ``space .. GB'' to the second column}
\end{table}
```

![table-multicol]({{site.url}}/latex-tricks/img/table/prefix.png)

### **Change space between columns:**


`\tabcolsep` changes the horizontal spacing between columns (Default = 6pt). 

`\arraystretch` changes the vertical spacing between rows (Default = 1, change it to the relative size). 

```
%%%% \tabcolsep changes the horizontal spacing between columns
\setlength{\tabcolsep}{20pt} % default = 6
%%%% \arraystretch changes the vertical spacing between rows
\renewcommand{\arraystretch}{1.5} % default = 1
```

You can also insert `@{}` around `clr` to specify the space around each cell. The default value is 4 spaces (`@{    }`). 


More generally, you can put anything in `@{}`. It will add this text to every column, but this text will replace the blanks between columns. You can also just put blanks into `@{}` to specify the number of blanks between columns. 

#### Example:

```
\begin{tabular}{@{Time: }l@{   Space: }l@{ }}
\end{tabular}
```

### Text Rotation

For rotating to vertical, simply use `sideway` to rotate for 90 degrees, or use the `rotating` package normally.

```
\begin{tabular}{ccc}
    \hline
    \multirow{3}{*}{\begin{sideways}\textbf{color}\end{sideways}} & red & abcdefg\\
    & blue & abcdefg\\
    & green & abcdefg\\
    \hline
    \multirow{2}{*}{\begin{turn}{45}\textbf{size}\end{turn}} & large & abcdefg\\
    & small & abcdefg\\
    \hline
\end{tabular}
```

![table-multicol]({{site.url}}/latex-tricks/img/table/rotating.png)

You can also use `sidewaystable` to put a horizontal table:

```
\begin{sidewaystable}
\end{sidewaystable}
```