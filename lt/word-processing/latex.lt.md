{
  "date": "2019-10-11",
  "keywords": [
"latekso failas",
"latekso failo formatas",
"kas yra latekso failas",
"failą",
"latekso pavyzdys",
"latekso failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LATEX – latekso dokumentų failas",
  "description": "Sužinokite apie LATEX failų formatą ir API, kurios gali kurti ir atidaryti LATEX failus.",
  "linktitle": "LATEX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-late-ltx"
}
},
  "lastmod": "2021-05-18"
}

## Kas yra LATEX failas?

Failas su plėtiniu .latex yra teksto žymėjimo kalbos failas, sukurtas naudojant rinkimo sistemą, vadinamą LaTex. Dažniausiai jis naudojamas apibrėžiant įvairių sričių leidinių, laiškų, knygų ir kitų panašių katalogų rinkinius. Latekso failo formatas pagerina dokumentą naudojant specializuotus algoritmus, dokumento formatavimo komandas ir smulkiausias detales. Tex failams atidaryti ir redaguoti galima naudoti latekso procesorius, tokius kaip TeXworks, Texmaker, LaTeX Editor, proTeXt ir Notepad++.

## LATEX failo formatas

LATEX failai yra paprasto teksto failai, kuriuos galima redaguoti bet kuriame teksto rengyklėje. Tekso rinkimo sistema plačiai naudojama akademinėje bendruomenėje, ypač matematikos, informatikos, ekonomikos, inžinerijos ir panašiose srityse. Jį sudaro komandų rinkinys, paprastai prasidedantis pasviruoju brūkšniu ir sugrupuotas su riestiniais skliaustais. Tex failo komentarai prasideda ir baigiasi dvigubais procentais (%%).

### LATEKSO pavyzdys

Toliau pateiktą turinį galima įklijuoti į tekstinį failą, kad būtų sukurtas paprastas LaTex dokumentas.

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

Aukščiau esančio komandos failo išvestis turėtų atrodyti taip:

{{< figure src="../latex-example.png" alt="Latekso failo formatas" >}}

## Nuorodos Nr.

* [TEX – Vikipedija](https://en.wikipedia.org/wiki/TeX)


