{
  "date" : "2019-10-11",
  "keywords" :[ "ltx-bestand", "ltx-bestandsindeling", "wat is een ltx-bestand", "bestand", "ltx-voorbeeld", "ltx-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - Latex-documentbestand",
  "description":"Meer informatie over de LTX-bestandsindeling en API's die LTX-bestanden kunnen maken en openen.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Wat is een LTX-bestand?

Een record met de extensie .ltx is een op een boek gebaseerd opmaaktaaldocument dat is gemaakt met het typesetting-framework dat bekend staat als LaTex. In een groot deel van de gevallen wordt het gebruikt om de typografieën voor distributies, brieven, boeken en andere vergelijkende opnames op verschillende gebieden te karakteriseren. Latex-recordontwerp verbetert het rapport met behulp van specifieke berekeningen, bestellingen voor het ordenen van het archief en de kleinste subtiliteiten. Latex-processors, bijvoorbeeld TeXworks, Texmaker, LaTeX Editor, proTeXt en Notepad++, kunnen worden gebruikt om Tex-records te openen en te wijzigen.

## LTX-bestandsindeling

LATEX-documenten zijn records in platte tekst die in elke tekstverwerker kunnen worden gewijzigd. Het Tex-typesetting-raamwerk wordt over het algemeen gebruikt in de wetenschappelijke gemeenschap, met name op het gebied van wiskunde, software-engineering, financiële aspecten, ontwerpen en dergelijke. Het bevat een aantal commando's die normaal beginnen met een schuine interpunctieregel (/nl/) en verzameld zijn met golvende steunen. Opmerkingen/opmerkingen in een LTX-bestand beginnen en eindigen met twee keer procent afbeeldingen (%%). LTX-bestanden lijken op de bestanden [.tex](/nl/page-description-language/tex/) en [.latex](/nl/word-processing/latex/) en u zult vaak latexdocumenten aantreffen die in deze indelingen zijn opgeslagen.

### LTX Voorbeeld

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
