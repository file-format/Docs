{
  "date" : "2019-10-11",
  "keywords" :[ "latex bestand", "latex bestandsformaat", "wat is een latex bestand", "bestand", "latex voorbeeld", "latex bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Latex documentbestand",
  "description":"Meer informatie over de LATEX-bestandsindeling en API's die LATEX-bestanden kunnen maken en openen.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Wat is een LATEX-bestand?

Een bestand met de extensie .latex is een op tekst gebaseerd opmaaktaalbestand dat is gemaakt met het zetsysteem dat bekend staat als LaTex. In de meeste gevallen wordt het gebruikt om de typografie voor publicaties, brieven, boeken en andere soortgelijke catalogisering op verschillende gebieden te definiëren. Latex-bestandsindeling verbetert het document met behulp van gespecialiseerde algoritmen, opdrachten voor het opmaken van het document en de kleinste details. Latex-processors zoals TeXworks, Texmaker, LaTeX Editor, proTeXt en Notepad++ kunnen worden gebruikt om Tex-bestanden te openen en te bewerken.

## LATEX-bestandsindeling

LATEX-bestanden zijn platte tekstbestanden die in elke teksteditor kunnen worden bewerkt. Het Tex-zetsysteem wordt veel gebruikt in de academische wereld, met name op het gebied van wiskunde, informatica, economie, techniek en soortgelijke anderen. Het bestaat uit een reeks opdrachten die gewoonlijk beginnen met een backslash en gegroepeerd met accolades. Opmerkingen in een tex-bestand beginnen en eindigen met dubbele procenttekens (%%).

### LATEX Voorbeeld

De volgende inhoud kan in een tekstbestand worden geplakt om een eenvoudig LaTex-document te maken.

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

De uitvoer van het bovenstaande opdrachtbestand zou er als volgt uit moeten zien:

{{< figure src="../latex-example.png" alt="Latex-bestandsindeling" >}}

## Referenties ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)
