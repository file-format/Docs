{
  "date" : "2019-10-11",
  "keywords" :[ "latex fájl", "latex fájlformátum", "mi az a latex fájl", "fájl", "latex példa", "latex fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Latex dokumentumfájl",
  "description":"További információ a LATEX fájlformátumról és az API-król, amelyek LATEX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Mi az a LATEX fájl?

A .latex kiterjesztésű fájl egy szövegalapú jelölőnyelvi fájl, amelyet a LaTex néven ismert betűszedő rendszerrel hoztak létre. Legtöbbször kiadványok, levelek, könyvek és más hasonló katalogizálás szedéseinek meghatározására szolgál különböző területeken. A latex fájlformátum speciális algoritmusok, a dokumentum formázására szolgáló parancsok és a legapróbb részletek segítségével javítja a dokumentumot. A latex processzorok, például a TeXworks, a Texmaker, a LaTeX Editor, a proTeXt és a Notepad++ használhatók a Tex fájlok megnyitására és szerkesztésére.

## LATEX fájlformátum

A LATEX fájlok egyszerű szöveges fájlok, amelyek bármilyen szövegszerkesztőben szerkeszthetők. A szövegszedő rendszert széles körben használják a tudományos életben, különösen a matematika, számítástechnika, közgazdaságtan, mérnöki tudományok és hasonló területeken. Ez egy sor parancsot tartalmaz, amelyek általában fordított perjellel kezdődnek, és kapcsos zárójelekkel vannak csoportosítva. A tex fájlban található megjegyzések dupla százalékjellel kezdődnek és végződnek (%%).

### LATEX Példa

A következő tartalom beilleszthető egy szöveges fájlba egy egyszerű LaTex dokumentum létrehozásához.

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

A fenti parancsfájl kimenetének így kell kinéznie:

{{< figure src="../latex-example.png" alt="Latex fájlformátum" >}}

## Referenciák ##

* [TEX – Wikipédia](https://en.wikipedia.org/wiki/TeX)
