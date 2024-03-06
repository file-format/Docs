{
  "date": "2019-10-11",
  "keywords": [
"ltx failu",
"ltx faila formātā",
"kas ir ltx fails",
"failu",
"ltx piemērs",
"ltx faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LTX — lateksa dokumentu fails",
  "description": "Uzziniet par LTX failu formātu un API, kas var izveidot un atvērt LTX failus.",
  "linktitle": "LTX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-lt-lvx"
}
},
  "lastmod": "2021-05-18"
}

## Kas ir LTX fails?

Ieraksts ar paplašinājumu .ltx ir uz grāmatām balstīts iezīmēšanas valodas dokuments, kas izveidots, izmantojot salikšanas sistēmu, kas pazīstama kā LaTex. Lielākajā daļā gadījumu to izmanto, lai raksturotu salikumus izplatījumiem, vēstulēm, grāmatām un citiem salīdzinošiem ierakstiem dažādās jomās. Lateksa ierakstu dizains pārskata atskaiti, izmantojot specifiskus aprēķinus, arhīva sakārtošanas pasūtījumus un mazākos smalkumus. Lai atvērtu un mainītu Tex ierakstus, var izmantot lateksa procesorus, piemēram, TeXworks, Texmaker, LaTeX Editor, proTeXt un Notepad++.

## LTX faila formāts

LATEX documents are plain text records that can be altered in any word processor. Tex typesetting framework is generally utilized in scholarly community particularly in the fields of math, software engineering, financial aspects, designing, and likewise others. It contains a bunch of commands normally beginning with an oblique punctuation line (/) and gathered with wavy supports. Remarks/comments in an LTX file start and end with twofold percent images (%%). LTX files are similar to [.tex](/page-description-language/tex/) and [.latex](/word-processing/latex/) file and you will often find latex documents saved in these formats.

### LTX piemērs

Lai izveidotu vienkāršu LaTex dokumentu, teksta failā var ielīmēt šādu saturu.

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

Iepriekš esošā komandu faila izvadei vajadzētu izskatīties šādi:

{{< figure src="../latex-example.png" alt="Lateksa faila formāts" >}}

## Atsauces Nr.

* [TEX — Wikipedia](https://en.wikipedia.org/wiki/TeX)


