{
  "date" : "2019-10-11",
  "keywords" :[ "latexfil", "latexfilformat", "vad är en latexfil", "fil", "latexexempel", "latexfiltillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Latex dokumentfil",
  "description":"Läs mer om LATEX-filformat och API:er som kan skapa och öppna LATEX-filer.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Vad är en LATEX fil?

En fil med tillägget .latex är en textbaserad märkningsspråkfil som skapats med det typsättningssystem som kallas LaTex. I de flesta fall används den för att definiera typinställningar för publikationer, brev, böcker och annan liknande katalogisering inom olika områden. Latexfilformatet förbättrar dokumentet med hjälp av specialiserade algoritmer, kommandon för formatering av dokumentet och de minsta detaljerna. Latexprocessorer som TeXworks, Texmaker, LaTeX Editor, proTeXt och Notepad++ kan användas för att öppna och redigera Tex-filer.

## LATEX filformat

LATEX-filer är vanliga textfiler som kan redigeras i vilken textredigerare som helst. Tex typsättningssystem används ofta inom akademin, särskilt inom områdena matematik, datavetenskap, ekonomi, teknik och liknande andra. Den består av en uppsättning kommandon som vanligtvis börjar med ett snedstreck och grupperas med hängslen. Kommentarer i en textfil börjar och slutar med dubbla procentsymboler (%%).

### LATEX Exempel

Följande innehåll kan klistras in i en textfil för att skapa ett enkelt LaTex-dokument.

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

Utdata från kommandofilen ovan bör se ut så här:

{{< figure src="../latex-example.png" alt="Latex filformat" >}}

## Referenser ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)
* [Latex](http://mally.stanford.edu/~sr/computing/latex-example.html)

