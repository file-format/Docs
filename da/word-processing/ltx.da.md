{
  "date": "2019-10-11",
  "keywords": [
"ltx fil",
"ltx filformat",
"hvad er en ltx-fil",
"fil",
"ltx eksempel",
"ltx filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LTX - Latex dokumentfil",
  "description": "Lær om LTX filformat og API'er, der kan oprette og åbne LTX filer.",
  "linktitle": "LTX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-lt-dax"
}
},
  "lastmod": "2021-05-18"
}

## Hvad er en LTX fil?

En post med .ltx-udvidelsen er et bogbaseret markup-sprogdokument lavet med den typesettingsramme kendt som LaTex. I en stor del af tilfældene bruges den til at karakterisere typesætningerne for distributioner, breve, bøger og anden sammenlignende optagelse i forskellige felter. Latex record design opgraderer rapporten ved at bruge specifikke beregninger, ordrer til at arrangere arkivet og de mindste finesser. Latex-processorer, for eksempel TeXworks, Texmaker, LaTeX Editor, proTeXt og Notepad++ kan bruges til at åbne og ændre Tex-poster.

## LTX filformat

LATEX documents are plain text records that can be altered in any word processor. Tex typesetting framework is generally utilized in scholarly community particularly in the fields of math, software engineering, financial aspects, designing, and likewise others. It contains a bunch of commands normally beginning with an oblique punctuation line (/) and gathered with wavy supports. Remarks/comments in an LTX file start and end with twofold percent images (%%). LTX files are similar to [.tex](/page-description-language/tex/) and [.latex](/word-processing/latex/) file and you will often find latex documents saved in these formats.

### LTX-eksempel

Følgende indhold kan indsættes i en tekstfil for at skabe et simpelt LaTex-dokument.

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

Outputtet af kommandofilen ovenfor skal se sådan ud:

{{< figure src="../latex-example.png" alt="Latex filformat" >}}

## Referencer ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)


