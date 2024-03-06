{
  "date": "2019-10-11",
  "keywords": [
"lateksa fails",
"lateksa faila formāts",
"kas ir lateksa fails",
"failu",
"lateksa piemērs",
"lateksa faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LATEX — lateksa dokumentu fails",
  "description": "Uzziniet par LATEX failu formātu un API, kas var izveidot un atvērt LATEX failus.",
  "linktitle": "LATEX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-late-lvx"
}
},
  "lastmod": "2021-05-18"
}

## Kas ir LATEX fails?

Fails ar paplašinājumu .latex ir uz tekstu balstīts iezīmēšanas valodas fails, kas izveidots ar salikšanas sistēmu, kas pazīstama kā LaTex. Vairumā gadījumu to izmanto, lai noteiktu salikumus publikācijām, vēstulēm, grāmatām un citai līdzīgai kataloģizēšanai dažādās jomās. Lateksa faila formāts uzlabo dokumentu, izmantojot specializētus algoritmus, komandas dokumenta formatēšanai un vissīkākās detaļas. Lai atvērtu un rediģētu Tex failus, var izmantot tādus lateksa procesorus kā TeXworks, Texmaker, LaTeX Editor, proTeXt un Notepad++.

## LATEX faila formāts

LATEX faili ir vienkārša teksta faili, kurus var rediģēt jebkurā teksta redaktorā. Teksa salikšanas sistēma tiek plaši izmantota akadēmiskajās aprindās, īpaši matemātikas, datorzinātņu, ekonomikas, inženierzinātņu un tamlīdzīgi citās jomās. Tas sastāv no komandu kopas, kas parasti sākas ar slīpsvītru un ir sagrupētas ar krokainajām iekavām. Komentāri teksta failā sākas un beidzas ar dubultajiem procentu simboliem (%%).

### LATEX Piemērs

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


