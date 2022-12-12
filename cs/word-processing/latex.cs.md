{
  "date" : "2019-10-11",
  "keywords" :[ "latexový soubor", "formát latexového souboru", "co je latexový soubor", "soubor", "příklad latexu", "přípona latexového souboru", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Latexový dokumentový soubor",
  "description":"Další informace o formátu souborů LATEX a rozhraních API, která mohou vytvářet a otevírat soubory LATEX.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Co je soubor LATEX?

Soubor s příponou .latex je textový soubor značkovacího jazyka vytvořený sázecím systémem známým jako LaTex. Ve většině případů se používá k definování sazby pro publikace, dopisy, knihy a další podobnou katalogizaci v různých oblastech. Formát souboru Latex vylepšuje dokument pomocí specializovaných algoritmů, příkazů pro formátování dokumentu a nejmenších detailů. Latexové procesory jako TeXworks, Texmaker, LaTeX Editor, proTeXt a Notepad++ lze použít k otevírání a úpravě souborů Tex.

## Formát souboru LATEX

Soubory LATEX jsou soubory ve formátu prostého textu, které lze upravovat v libovolném textovém editoru. Sázecí systém Tex je široce používán v akademické sféře zejména v oblastech matematiky, informatiky, ekonomie, strojírenství a podobně. Skládá se ze sady příkazů obvykle začínajících zpětným lomítkem a seskupených do složených závorek. Komentáře v souboru tex začínají a končí symboly dvou procent (%%).

### Příklad LATEXu

Následující obsah lze vložit do textového souboru a vytvořit jednoduchý dokument LaTex.

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

Výstup příkazového souboru výše by měl vypadat takto:

{{< figure src="../latex-example.png" alt="Formát souboru Latex" >}}

## Reference ##

* [TEX - Wikipedie](https://en.wikipedia.org/wiki/TeX)
* [Latex](http://mally.stanford.edu/~sr/computing/latex-example.html)

