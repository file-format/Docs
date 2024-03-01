{
  "date": "2019-10-11",
  "keywords": [
"lateksi tiedosto",
"lateksi tiedostomuoto",
"mikä on lateksitiedosto",
"tiedosto",
"esimerkki lateksista",
"latex tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LATEX - Latex-asiakirjatiedosto",
  "description": "Opi LATEX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata LATEX-tiedostoja.",
  "linktitle": "LATEX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-late-fix"
}
},
  "lastmod": "2021-05-18"
}

## Mikä on LATEX-tiedosto?

Tiedosto, jonka pääte on .latex, on tekstipohjainen merkintäkielitiedosto, joka on luotu LaTex-nimisen ladontajärjestelmän avulla. Useimmissa tapauksissa sitä käytetään julkaisujen, kirjeiden, kirjojen ja muiden vastaavien eri alojen luettelointien määrittämiseen. Lateksitiedostomuoto parantaa asiakirjaa käyttämällä erikoisalgoritmeja, dokumentin muotoilukomentoja ja pienimpiä yksityiskohtia. Lateksiprosessoreita, kuten TeXworks, Texmaker, LaTeX Editor, proTeXt ja Notepad++, voidaan käyttää Tex-tiedostojen avaamiseen ja muokkaamiseen.

## LATEX-tiedostomuoto

LATEX-tiedostot ovat pelkkiä tekstitiedostoja, joita voidaan muokata missä tahansa tekstieditorissa. Tex-ladontajärjestelmää käytetään laajalti yliopistomaailmassa erityisesti matematiikan, tietojenkäsittelytieteen, taloustieteen, tekniikan ja vastaavien aloilla. Se koostuu joukosta komentoja, jotka alkavat tavallisesti kenoviivalla ja ryhmitellään kiharoilla aaltosulkeilla. Tex-tiedoston kommentit alkavat ja päättyvät kaksinkertaisilla prosenttisymboleilla (%%).

### LATEX Esimerkki

Seuraava sisältö voidaan liittää tekstitiedostoon yksinkertaisen LaTex-asiakirjan luomiseksi.

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

Yllä olevan komentotiedoston tulosteen pitäisi näyttää tältä:

{{< figure src="../latex-example.png" alt="Latex-tiedostomuoto" >}}

## Viitteet ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)


