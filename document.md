# What is LaTeX?

## Table Of Contents

- Document structure
- [LaTeX command instructions](https://github.com/dghuuloc/Full-Stack/tree/main/contents/latex/commands)
- Document Preambles
- Adding a Title, Author, and Date
- Adding a Comment
- Adding Bold, Italics, and Underlining
- Adding images
- Reamble of a Document
- Captions, labels and references
- Creating Lists
- Creating Tables
- Macros
- Adding Math
- Abstracts
- Chapters and Sections
- Captions, labels and references
- Packages and Classes
- Adding a Tables of Contents

---

## Document structure

``` latex
\documentclass{article}

\begin{document}
Welcome to LaTeX!

\end{document}

```

## Document Preambles

``` latex
\documentclass[12pt, a4paper, twoside]({article}
\usepackage[utf8]{inputenc}
```

## Adding a Title, Author, and Date

``` latex
\title{Chapter one}
\author{Created by ...\thanks{sponsored by the Resurchify team}}
\date{Jan 2022}
```

This should be included in the body of the document, at the place you want the title to appear. With this code:

``` latex
\documentclass{article}
\usepackage[utf8]{inputenc}

\title{My Example}
\author{Maxine Meurer}
\date{July 2021}

\begin{document}

\maketitle

You're on your way to creating your \LaTeX{} document!

\end{document}
```
To get the title, name of author and date in the document, use `\maketitle` command. This has to be included in the body of the document where the title has to be printed.

## Adding a Comment

To make a comment in LaTeX, just write a `%` symbol at the beginning of the line like so:

``` latex
%Let's change the font size again later!
```

## Adding Bold, Italics, and Underlining



So for the example:

``` latex
Let's \textbf{bold} some text!
Let's \underline{underline} some text!
let's italicize \textbf{AND} bold \textbf{\textit{some text}
```
Another formatting command is `\emph{...}` command. Its activity depends on the context. For normal text, it makes it italic. And the process is reversed if it is applied on italicized text. 

For example,

``` latex
Some of the greatest \emph{discoveries} in science  were made by accident.
\textit{Some of the greatest \emph{discoveries} in science were made
by accident.}
\textbf{Some of the greatest \emph{discoveries} in science were made
by accident.}
```

## Creating Lists

### Unordered Lists

``` latex
\begin{itemize}
  \item Yay, my first list item.
  \item Lets get to work.
\end{itemize}
```

### Ordered Lists

``` latex
\begin{enumerate}
  \item Yay, my first list item.
  \item Lets get to work.
\end{enumerate}
```
## References

[LaTeX Tutorial: Learn LaTeX Step by Step](https://www.resurchify.com/latex_tutorial/latex_quick_guide.php)

[A simple guide to LaTeX – Step by Step](https://latex-tutorial.com/tutorials/)

[resume-generator](https://github.com/ayan-b/resume-generator/blob/master/config/data.yml)

[My experience writing a CV so far](https://dev.to/vulwsztyn/my-experience-writing-a-cv-so-far-24eb)
[LaTeX Example](https://alvinalexander.com/blog/post/latex/create-your-own-commands-in-latex-using-newcommand/)
[The Fontawesome](https://mirrors.ibiblio.org/CTAN/fonts/fontawesome5/doc/fontawesome5.pdf)
