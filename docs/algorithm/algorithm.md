---
layout: default
title: Algorithms
has_children: true
nav_order: 5
---

## **Algorithms**

Use the package with commonly-used options as follows. [[document]](https://mirror2.sandyriver.net/pub/ctan/macros/latex/contrib/algorithm2e/doc/algorithm2e.pdf)

```
\usepackage[ruled,lined,linesnumbered,noend]{algorithm2e}
\usepackage[noend]{algpseudocode}
```

A quick example:

```
%% settings
\SetSideCommentLeft
% use \notations{...} or \notes{...} etc.
\SetKwInput{notations}{Notations}
\SetKwInput{notes}{Notes}
\SetKwInput{maintains}{Maintains}

% use \myfunc(right-aligned comment){function name}{...function content...}
\SetKwProg{myfunc}{Function}{}{}
% use \parForEach as a regular \For
\SetKwFor{parForEach}{ParallelForEach}{do}{endfor}
\SetKwFor{Justrepeat}{Repeat}{}{}
% CommentStyle
\newcommand\mycommfont[1]{\textit{\textcolor{blue}{#1}}}
\SetCommentSty{mycommfont}
%% end settings

\begin{algorithm}[t]
\caption{Compute something}\label{algo:algo}
\KwIn{This is the input}
\KwOut{This is the output}
\notes{Some notes}
do something \\
\While{something}{ do something }
\lWhile{something}{ %while loop in one line
    do something }
\For{$i$ from 0 to $n$}{
    do something\\
    do more things }
\lFor{$i$ from 0 to $n$}{ %for loop in one line
    do something }
\If(\tcp*[f]{comment}){something is true} {do A}
\Else{do B}
\lIf{something is true} {do A} %If in one line
\lElse{do B} %Else in one line
\leIf{condition}{do A}{do B}
do something \tcp{this is some short comment}
\tcc{this is a long comment, which can be very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, very, long.}
$a\gets b+c$\\
\Justrepeat{}{
This repeat does not have an until
}
\parForEach{$i\gets 1$ to $n$}{
  $a[i]\gets a[i]+1$
}
\Return{your return value}
\end{algorithm}
```

![algo-basic]({{site.url}}/latex-tricks/img/algorithm/basic.png)

### **Commonly used keywords**

```
\KwIn{input description}
\KwOut{output description}
\If{condition}{then statement}
\Else{else statement}
\eIf{condition}{then statement}{else statement}
\Return{return value}
\For{loop condition}{body}
\ForEach{loop condition}{body}
\While{condition}{body}
\Repeat{end condition}{body}
```

Add `l` in front of any keyword to make it one line. For example:

```
% If and then-statement in one line
\lIf{condition}{then statement} 
% Else and else-statement in one line
\lElse{else statement}
% if-then-else all in one line
\leIf{condition}{then statement}{else statement}
```

Many other usages are specified in the document. 

To define new keywords, see [algorithm/keywords](/latextrics/docs/algorithm/keywords.html)


### **Comments**

Some options:

`\SetSideCommentLeft`: side comments are flushed to the right

`\SetSideCommentRight`: side comments right after code (so more to the left)

`\SetFillComment`: comment fill a line so the end of comment symbol is pushed to the right

`\SetNoFillComment`: comment ends immediately so the end of comment symbol is right after the comment

Comment types:

`\tcc{comment}`: line(s) of comment. Comment "la" C (`/* ... */`) in blocks

`\tcc*{comment}`: side comment. Comment "la" C (`/* ... */`) but put at the right of the code

`\tcp{comment}`: line(s) of comment. Comment "la" C++ (`//...`) in blocks

`\tcp*{comment}`: side comment. Comment "la" C++ (`//...`) but put at the right of the code

`\tcp*[f]{comment}`: side comment. Comment "la" C++ (`//...`). Without new line. Useful in if-then-else/for/while/... macros. 

For some keywords, put `(comment)` after the keyword to add right-aligned comments. 

```
\If(\tcp*[f]{comment}){something is true}{do something}
```

Here `comment` will show up on the same line as `if` but to the right. Similarly this can be used for `for`, `while`, etc. It is especially useful when these statements are put in one line (`lWhile`, `lIf`, ...).

Define comment style as:

```
% CommentStyle
\newcommand\mycommfont[1]{\textit{\textcolor{blue}{#1}}}
\SetCommentSty{mycommfont}
```

Many other usages of comments and special styles are specified in the document. 