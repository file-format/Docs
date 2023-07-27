{
  "date" : "2019-10-11",
  "keywords" :[ "file ltx", "formato file ltx", "cos'è un file ltx", "file", "esempio ltx", "estensione file ltx", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - File di documenti in lattice",
  "description":"Scopri il formato di file LTX e le API che possono creare e aprire file LTX.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Che cos'è un file LTX?

Un record con estensione .ltx è un documento del linguaggio di markup basato su libri realizzato con il framework di composizione noto come LaTex. In gran parte dei casi, viene utilizzato per caratterizzare la composizione tipografica per distribuzioni, lettere, libri e altre registrazioni comparative in diversi campi. Il design del record in lattice aggiorna il rapporto utilizzando calcoli specifici, ordini per l'organizzazione dell'archivio e le più piccole sottigliezze. I processori in lattice, ad esempio TeXworks, Texmaker, LaTeX Editor, proTeXt e Notepad++, possono essere utilizzati per aprire e modificare i record Tex.

## Formato file LTX

I documenti LATEX sono record di testo semplice che possono essere modificati in qualsiasi elaboratore di testi. Il framework di composizione del testo è generalmente utilizzato nella comunità accademica, in particolare nei campi della matematica, dell'ingegneria del software, degli aspetti finanziari, della progettazione e simili. Contiene una serie di comandi che normalmente iniziano con una linea di punteggiatura obliqua (/it/) e sono raccolti con supporti ondulati. Le osservazioni/commenti in un file LTX iniziano e finiscono con il doppio delle immagini percentuali (%%). I file LTX sono simili ai file [.tex](/it/page-description-language/tex/) e [.latex](/it/word-processing/latex/) e spesso troverai documenti in lattice salvati in questi formati.

### Esempio LTX

Il seguente contenuto può essere incollato in un file di testo per creare un semplice documento LaTex.

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

L'output del file di comando sopra dovrebbe essere simile a questo:

{{< figure src="../latex-example.png" alt="Formato file in lattice" >}}

## Riferimenti ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)
