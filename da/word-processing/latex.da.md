{
  "date": "2019-10-11",
  "keywords": [
"latex fil",
"latex filformat",
"hvad er en latex fil",
"fil",
"latex eksempel",
"latex filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LATEX - Latex dokumentfil",
  "description": "Lær om LATEX filformat og API'er, der kan oprette og åbne LATEX filer.",
  "linktitle": "LATEX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-late-dax"
}
},
  "lastmod": "2021-05-18"
}

## Hvad er en LATEX fil?

En fil med filtypenavnet .latex er en tekstbaseret opmærkningssprogfil, der er oprettet med det typesætningssystem, der er kendt som LaTex. I de fleste tilfælde bruges det til at definere typeindstillingerne for publikationer, breve, bøger og anden lignende katalogisering på forskellige områder. Latex filformat forbedrer dokumentet ved hjælp af specialiserede algoritmer, kommandoer til formatering af dokumentet og de mindste detaljer. Latex-processorer som TeXworks, Texmaker, LaTeX Editor, proTeXt og Notepad++ kan bruges til at åbne og redigere Tex-filer.

## LATEX filformat

LATEX-filer er almindelige tekstfiler, der kan redigeres i enhver teksteditor. Tex sætningssystem er meget udbredt i den akademiske verden, især inden for matematik, datalogi, økonomi, teknik og lignende andre. Den består af et sæt kommandoer, der almindeligvis starter med en omvendt skråstreg og grupperet med krøllede seler. Kommentarer i en tekstfil starter og slutter med dobbelte procentsymboler (%%).

### LATEX Eksempel

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


