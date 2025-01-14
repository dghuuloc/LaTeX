# <p align="center">LaTeX Beginner's Guide</p>
---

### What are LaTeX Packages?
A basic TeX distribution doesn't actually provide much functionality. In most cases, creating a LaTeX document will require packages that provide additional options or functionality. The packages generally come into use when you want to insert an image or graphics, colored texts, or a source code from a file into a document, etc.

Packages required by a document are called in the __preamble__ of your LaTeX document, i.e. before the `\begin{document}` statement. The syntax to do so is `\usepackage[options]{package_name}`, with the name of the package included in the brackets.

### Understanding LaTeX Commands
LaTeX commands begin with a backslash, followed by big or small letters, and are usually named in a descriptive way.

Commands can have __parameters__, that is, options that determine in which way the command does its work. The values that we hand over as parameters are called __arguments__. They are given in curly braces or square brackets, as we will explain now.

So, calling a command can look like this:

```tex
\commandname[optional argument]{main argument}
```
Note, that all commands must be proceeded by the backslash mark and the main argument must be included inside `{..}` pair.

Some commands have more than one arguments, for example:
```tex
\multicolumn{number of columns joined}{alignment}{content} 
```

Some commands do not need {} pair to work well, for example:
```tex
\item Text being item content
```
> [!NOTE]
> __Commands, macros, and declarations__
> 
> Most LaTex commands, including those we define ourselves, consist of other commands. That's why LaTeX commands are also called __macros__, and the terms _macro_ and _command_ are used interchangeably. A command or macro the doesn't print something but just changes current settings, such as the font shape or text alignment, is also called a __declaration__.

### Understanding LaTeX Environments
Environment is a special type of command. LaTeX environments start with `\begin` and end with `\end`. Both commands require the name of the environment as their argument.

General environment structure is as following:
```tex
\begin{environmentname}[optional argument]{main argument}
  ...
\end{environmentname}
```
Some environments take arguments and optional arguments, like commands. For example
```tex
\begin{tabular}[table position]{column specifications}
 table content
\end{tabular}
```

### The preamble of a document
The preamble in a LaTeX document is the space between the `\documentclass` and `\begin{document}` commands where you define the document class, include packages, specify properties, set page layout, and define custom commands. For example:

```tex
\documentclass[12pt, a4paper, twoside]{article}
\usepackage[utf8]{inputenc}
\usepackage[margin=1in]{geometry}
\usepackage{hyperref}
\newcommand{\mycommand}[1]{\textcolor{red}{#1}}
```

> [!NOTE]
> In this section of the text file you will tell LaTeX about all the tools that you need to use:
> - Packages
> - Commands
> - Files


### The main body of the document
The body of the document should be placed between the `\begin{document}` and `\end{document}` commands, anything after the `\end{document}` command will be ignored.

```tex
\documentclass[12pt, a4paper, twoside]{article}
\usepackage[utf8]{inputenc}
\usepackage[margin=1in]{geometry}
\usepackage{hyperref}
\newcommand{\mycommand}[1]{\textcolor{red}{#1}}

% start main body of document
\begin{document}
This is my first document in LaTeX.
\end{document}
% end main body of document
```
### Top Matter

The LaTeX engine defines the document and author information as Top Matter. Although there does not exist any command as such `\topmatter`, the top matter includes document information like title, date, and author information like name, email, etc.
A standard article will begin with a document title, followed by author names and addresses. The code to obtain these are:
```tex
\begin{document}
\title{Title of the document}
\author{Donald Knuth and Leslie Lamport \cr
{Address of Authors}
\date{\today}
\maketitle
\end{document}
```
Here, `\cr` is used for breaking the line after the names in `\author`. The document date can be simply changed by writing the date in it, for example, `\date{30 August 2021}`, or the date can be ignored by leaving its content empty, i.e., \date{}.

### Single line or multi-line comments in LaTeX
#### Sinngle line comment in LaTeX
In case of single-line comment, you need to use percent symbol `(%)`.
```tex
% This is a multiline comment in LaTeX
% You can use the % symbol at the beginning of each line
\documentclass{article}
\begin{document}
\noindent Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse pretium nibh turpis. Donec nec magna neque. Pellentesque metus urna, volutpat at risus et, euismod hendrerit ex. Vestibulum semper quis metus in pretium.

% The following lines are commented out
% This is line 1 of the comment
% This is line 2 of the comment
% This is line 3 of the comment

\end{document}
```
#### Multi-line comments in LaTeX

___Using `iffalse` and `fi` commands___

`\iffalse` and `\fi` commands can be used to create a block comment. Anything between `\iffalse` and `\fi` will be ignored by the compiler.

```tex
\documentclass{article}
\begin{document}
\noindent Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse pretium nibh turpis. Donec nec magna neque. Pellentesque metus urna, volutpat at risus et, euismod hendrerit ex. Vestibulum semper quis metus in pretium.

\iffalse
    This is a multiline comment in LaTeX.
    You can use \iffalse and \fi to comment out multiple lines.
    These lines will be ignored during compilation.
\fi

\end{document}
```
___Use comment package___

`comment` package provides a convenient way to create block comments. But, Remember to include the `\usepackage{comment}` line in preamble of your document.
```tex
\documentclass{article}
\usepackage{comment}
\begin{document}
\noindent Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Proin finibus vestibulum feugiat. Phasellus a enim aliquet, cursus magna ut, bibendum tellus. Integer nibh magna, sollicitudin at dui quis, ullamcorper varius leo. \\[6pt]

\begin{comment}
    This is a block comment using the comment package.
    You can include as many lines as you want in this block,
    and they will be ignored during compilation.
\end{comment}

\noindent Nulla malesuada facilisis dui, quis auctor ante facilisis convallis. Ut bibendum luctus massa, a molestie arcu tempor id. Maecenas faucibus congue eros ac convallis. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Cras vel purus odio. 
\end{document}

```

### Abstract and Keywords
While writing research papers it is mandatory to include the abstract and the keywords before the main section of the body. The LaTeX engine bears pre-defined commands that inform it what part of content makes up the abstract and keywords respectively. The command to include abstract and keywords in the document exist for document class like article and report, however, not available for book class of document.

Immediately after the Title part, the Abstract and Keywords can be added as follows:

```tex
\begin{abstract}
  Abstract text goes here ... a
  Keywords: keyword; keyword; keyword
\end{abstract}
```

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


### Structure of the document
To define the hierarchical structure of the document LaTeX provides special commands that defines chapter, section, etc.

```tex
\part[part short title]{part title}
```
```tex
\chapter[chapter short title]{chapter title}
```
```tex
\section[section short title]{section title}
```
```tex
\subsection[subsection short title]{subsection title}
```
```tex
\subsubsection[subsubsection short title]{subsubsection title}
```
```tex
\paragraph[paragraph short title]{paragraph title}
```
```tex
\subparagraph[subparagraph short title]{subparagraph title}
```
>[!WARNING]
> The first option of commands, which is placed within square brackets `[]`, is optional and can be utilized to change the name of the section that will be displayed in the Table of Contents, if necessary.

LaTeX will automatically number the chapters, parts, sections, etc. You can use `(*)` symbol sign after the section commands if you don’t want certain sections to be numbered. Additionally, using the `(*)` sign after the section commands will not reflect that particular section in the table of contents, too.

```tex
\section*{My First Section Title}
\subsection*{My First Subsection Title}
```

### Fonts in Documents
```tex
\documentclass[12pt]{article}
\usepackage{fontspec}
 
\setmainfont{Times New Roman}
\title{Sample font document}
\author{dghuuloc}
\date{\today}
   
\begin{document}
\maketitle

\setmainfont{Times New Roman}
Sử dụng Font Times New Roman cho việc gõ tiếng Việt
     
This is an \textit{example} of a document compiled 
with \textbf{LuaLaTeX}.

\setmainfont{Latin Modern Sans}
How to use latin Modern Sans Fonts

\end{document}
```

```tex
\documentclass[a4paper, 12pt]{article}
\usepackage[utf8]{inputenc}

\usepackage[main=vietnamese, english]{babel}
% \usepackage[T5]{fontenc}
% \usepackage[utf8]{vietnam}

\title{Sample font document}
\author{dghuuloc}
\date{\today}
   
\begin{document}
\maketitle

Hà Nội là thủ đô, đồng thời là thành phố đứng đầu Việt Nam về diện
tích tự nhiên và đứng thứ hai về diện tích đô thị sau thành phố Hồ Chí
Minh.

\end{document}
```

### References
- [LaTeX Quickstart](https://www.texready.ir/docs/quickstart)
- [Learn LaTeX — A Beginner's Step-By-Step Guide](https://typeset.io/resources/learn-latex-beginners-step-by-step-guide/)
- [UTF-8](https://tex.stackexchange.com/questions/507109/how-can-i-use-utf-8vietnamese-in-equation-environment)
- [Foreign language](https://tex.stackexchange.com/questions/644783/table-captions-default-to-foreign-language)
