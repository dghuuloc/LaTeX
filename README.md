# LateX

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
