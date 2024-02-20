{
  "date": "2019-10-11",
  "keywords": [
    "latex file",
    "latex file format",
    "what is an latex file",
    "file",
    "latex example",
    "latex file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "LATEX - Latex Document File",
  "description": "Learn about LATEX file format and APIs that can create and open LATEX files.",
  "linktitle": "LATEX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-latex"
    }
  },
  "lastmod": "2021-05-18"
}

## What is a LATEX file?

A file with .latex extension is a text-based markup language file created with the typesetting system known as LaTex. In most of the cases, it is used to define the typesettings for publications, letters, books, and other similar cataloging in various fields. Latex file format enhances the document using specialized algorithms, commands for formatting of the document, and the tiniest details. Latex processors such as TeXworks, Texmaker, LaTeX Editor, proTeXt, and Notepad++ can be used to open and edit Tex files.

## LATEX File Format

LATEX files are plain text files that can be edited in any text editor. Tex typesetting system is widely used in academia especially in the fields of mathematics, computer science, economics, engineering, and similarly others. It comprises of a set of commands commonly starting with a backslash and grouped with curly braces. Comments in a tex file start and end with double percent symbols (%%).

### LATEX Example

The following content can be pasted in a text file to create a simple LaTex document.

```
\documentclass[12pt]{article}
\usepackage{lingmacros}
\usepackage{tree-dvips}
\begin{document}

\section*{Notes for My Paper}

Don't forget to include examples of topicalization.
They look like this:

{\small
\enumsentence{Topicalization from sentential subject:\\
\shortex{7}{a John$_i$ [a & kltukl & [el &
  {\bf l-}oltoir & er & ngii$_i$ & a Mary]]}
{ & {\bf R-}clear & {\sc comp} &
  {\bf IR}.{\sc 3s}-love   & P & him & }
{John, (it's) clear that Mary loves (him).}}
}

\subsection*{How to handle topicalization}

I'll just assume a tree structure like (\ex{1}).

{\small
\enumsentence{Structure of A$'$ Projections:\\ [2ex]
\begin{tabular}[t]{cccc}
    & \node{i}{CP}\\ [2ex]
    \node{ii}{Spec} &   &\node{iii}{C$'$}\\ [2ex]
        &\node{iv}{C} & & \node{v}{SAgrP}
\end{tabular}
\nodeconnect{i}{ii}
\nodeconnect{i}{iii}
\nodeconnect{iii}{iv}
\nodeconnect{iii}{v}
}
}

\subsection*{Mood}

Mood changes when there is a topic, as well as when
there is WH-movement.  \emph{Irrealis} is the mood when
there is a non-subject topic or WH-phrase in Comp.
\emph{Realis} is the mood when there is a subject topic
or WH-phrase.

\end{document}
```

The output of the command file above should look like this:

{{< figure src="../latex-example.png" alt="Latex File Format" >}}

## References ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)
