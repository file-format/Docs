{
  "date" : "2019-10-11",
  "keywords" :[ "ltx-fil", "ltx-filformat", "vad är en ltx-fil", "fil", "ltx-exempel", "ltx-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - Latex dokumentfil",
  "description":"Läs mer om LTX-filformat och API:er som kan skapa och öppna LTX-filer.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Vad är en LTX fil?

En post med .ltx-tillägget är ett bokbaserat märkningsspråksdokument som gjorts med typsättningsramverket känt som LaTex. I en stor del av fallen används den för att karakterisera typsättningarna för distributioner, brev, böcker och annan jämförande inspelning inom olika områden. Utformningen av latexskivor uppgraderar rapporten med hjälp av specifika beräkningar, beställningar för att ordna arkivet och de minsta finesser. Latexprocessorer, till exempel TeXworks, Texmaker, LaTeX Editor, proTeXt och Notepad++ kan användas för att öppna och ändra Tex-poster.

## LTX filformat

LATEX-dokument är vanliga textposter som kan ändras i vilken ordbehandlare som helst. Tex typsättningsramverk används vanligtvis i forskarsamhället, särskilt inom områdena matematik, mjukvaruteknik, ekonomiska aspekter, design och likaså andra. Den innehåller ett gäng kommandon som normalt börjar med en sned skiljeteckenlinje (/sv/) och samlas med vågiga stöd. Anmärkningar/kommentarer i en LTX-fil börjar och slutar med tvåfaldig procent av bilder (%%). LTX-filer liknar filen [.tex](/sv/page-description-language/tex/) och [.latex](/sv/ord-processing/latex/) och du hittar ofta latexdokument sparade i dessa format.,

### LTX-exempel

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

