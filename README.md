# <p align="center">LaTeX Beginner's Guide</p>
---

### What are LaTeX Packages?
A basic TeX distribution doesn't actually provide much functionality. In most cases, creating a LaTeX document will require packages that provide additional options or functionality. The packages generally come into use when you want to insert an image or graphics, colored texts, or a source code from a file into a document, etc.

Packages required by a document are called in the __preamble__ of your LaTeX document, i.e. before the `\begin{document}` statement. The syntax to do so is `\usepackage[options]{package_name}`, with the name of the package included in the brackets.

### Text Effects
If you want to emphasise text, you can use the `\emph{}` command, which will emphasise the text in between the curly brackets, usually by putting it in italics. You can also specify this and other effects more directly:

- `\emph{}` emphasises text (usually italicised)
- `{\em some_text }` also emphasises text (usually italicised) but note the different placing of brackets!
- `{\bf some_text }` emboldens text but note the different placing of brackets!
- `\textrm{}` sets text in the `normal Roman font`
- `\textit{}` sets text in `italic` typeface
- `\textbf{}` sets text in `bold` typeface
- `\texttt{}` sets text in the `typewriter font family`, fixed-width fount
- `\textsc{}` sets text in the `small capitals` typeface; everything will be in uppercase, but any capital letters will be typeset slightly bigger than the normal letters
- `\textnormal{}` sets text in the `document font family`
- `\textsf{}` sets text in the `sans sefiffont family`
- `\textup{}` sets text in the `upright shape`
- `\textsl{}` sets text in the `slated shape`
- `\textmd{}` sets text in the `normal weight and width`

### Paragraph Alignment

| Alignment         | Environment        | Command           |
| :---------------- | :----------------: | :---------------- |
| Left justified    | flushleft          | \raggedright      |
| Right justified   | flushright         | \raggedleft       |
| Center            | center             | \centering        |

### List structures
List often appear in documents, especially academic, as their purpose is often to present information in a clear and concise fashion. List structures in LaTeX are simply environments which essentially come in three flavours: itemize, enumerate and description.

All list follow the basic format:
```tex
\begin{list_type}
  \item The first item
  \item The second item
  \item The third item etc \ldots
\end{list_type}
```

#### Itemize
This environment is for your standard bulleted list of items

```tex
\begin{itemize}
  \item The first item
  \item The second item
  \item The third etc \ldots
\end{itemize}
```

#### Enumerate
The enumerate environment is for ordered lists, where by default, each item is numbered sequentially.

```tex
\begin{enumerate}
  \item The first item
  \item The second item
  \item The third etc \ldots
\end{enumerate}
```

#### Description
The description environment is slightly different. You can specify the item label by passing it as an optional argument (although optional, it would look odd if you didn't include it!). Ideal for a series of definitions, such as a glossary.

```tex
\begin{description}
  \item[First] The first item
  \item[Second] The second item
  \item[Third] The third etc \ldots
\end{description}
```

#### Nested List
LaTeX will happily allow you to insert a list environment into an existing one (up to a depth of four). Simply begin the appropriate environment at the desired point within the current list. LaTeX will sort out the layout and any numbering for you.

```tex
\begin{enumerate}
  \item The First item
  \begin{enumerate}
    \item Nested item 1
    \item Nested item 2
  \end{enumerate}
  \item The second item
  \item The thirds etc \ldots
\end{enumerate}
```


### Formatting documents and text
#### Sections
LaTeX can organize documents into chapters and sections. Levels of depth are:

```tex
\part{}
\chapter{}
\section{}
\subsection{}
\subsubsection{}
\paragraph{}
\subparagraph{}
```
