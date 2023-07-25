{
  "date" : "2019-10-11",
  "keywords" :[ "file in lattice", "formato file in lattice", "cos'è un file in lattice", "file", "esempio in lattice", "estensione file in lattice", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - File di documento in lattice",
  "description":"Scopri il formato di file LATEX e le API che possono creare e aprire file LATEX.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Che cos'è un file LATEX?

Un file con estensione .latex è un file di linguaggio di markup basato su testo creato con il sistema di composizione noto come LaTex. Nella maggior parte dei casi, viene utilizzato per definire la composizione tipografica di pubblicazioni, lettere, libri e altre catalogazioni simili in vari campi. Il formato file Latex migliora il documento utilizzando algoritmi specializzati, comandi per la formattazione del documento e i minimi dettagli. Processori Latex come TeXworks, Texmaker, LaTeX Editor, proTeXt e Notepad++ possono essere utilizzati per aprire e modificare file Tex.

## Formato file LATEX

I file LATEX sono file di testo semplice che possono essere modificati in qualsiasi editor di testo. Il sistema di composizione Tex è ampiamente utilizzato nel mondo accademico, specialmente nei campi della matematica, dell'informatica, dell'economia, dell'ingegneria e simili. Comprende una serie di comandi che iniziano comunemente con una barra rovesciata e raggruppati tra parentesi graffe. I commenti in un file tex iniziano e finiscono con simboli di doppia percentuale (%%).

### Esempio di LATEX

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
