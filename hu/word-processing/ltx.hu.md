{
  "date" : "2019-10-11",
  "keywords" :[ "ltx fájl", "ltx fájlformátum", "mi az ltx fájl", "fájl", "ltx példa", "ltx fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - Latex dokumentumfájl",
  "description":"További információ az LTX fájlformátumról és az LTX-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Mi az LTX fájl?

A .ltx kiterjesztésű rekord egy könyv alapú jelölőnyelvi dokumentum, amely a LaTex néven ismert betűszedő keretrendszerrel készült. Az esetek nagy részében a terjesztések, levelek, könyvek és egyéb összehasonlító felvételek szedéseinek jellemzésére használják különböző területeken. A latex rekordtervezés speciális számítások, archívumrendezési utasítások és a legapróbb finomságok felhasználásával frissíti a jelentést. A latex processzorok, például a TeXworks, a Texmaker, a LaTeX Editor, a proTeXt és a Notepad++ használhatók a Tex rekordok megnyitására és módosítására.

## LTX fájl formátum

A LATEX dokumentumok egyszerű szöveges rekordok, amelyek bármilyen szövegszerkesztőben módosíthatók. A szövegszedési keretrendszert általában a tudományos közösségben használják, különösen a matematika, a szoftverfejlesztés, a pénzügyi szempontok, a tervezés és hasonló területeken. Egy csomó parancsot tartalmaz, amelyek általában ferde írásjellel (/hu/) kezdődnek, és hullámos támaszokkal vannak összegyűjtve. Az LTX-fájlok megjegyzései/megjegyzései kétszeres százalékos képekkel kezdődnek és végződnek (%%). Az LTX fájlok hasonlóak a [.tex](/hu/page-description-language/tex/) és [.latex](/hu/word-processing/latex/) fájlokhoz, és gyakran találhat ilyen formátumban mentett latex dokumentumokat.

### LTX példa

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

## Hivatkozások ##

* [TEX – Wikipédia](https://en.wikipedia.org/wiki/TeX)
* [Latex](http://mally.stanford.edu/~sr/computing/latex-example.html)

