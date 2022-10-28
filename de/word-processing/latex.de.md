{
  "date" : "2019-10-11",
  "keywords" :[ "Latexdatei", "Latexdateiformat", "Was ist eine Latexdatei", "Datei", "Latexbeispiel", "Latexdateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Latex-Dokumentdatei",
  "description":"Erfahren Sie mehr über das LATEX-Dateiformat und APIs, die LATEX-Dateien erstellen und öffnen können.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Was ist eine LATEX-Datei?

Eine Datei mit der Erweiterung .latex ist eine textbasierte Markup-Sprachdatei, die mit dem als LaTex bekannten Schriftsatzsystem erstellt wurde. In den meisten Fällen wird es verwendet, um die Schriftsätze für Veröffentlichungen, Briefe, Bücher und andere ähnliche Katalogisierungen in verschiedenen Bereichen zu definieren. Das Latex-Dateiformat verbessert das Dokument mit speziellen Algorithmen, Befehlen zur Formatierung des Dokuments und den kleinsten Details. Latex-Prozessoren wie TeXworks, Texmaker, LaTeX Editor, proTeXt und Notepad++ können zum Öffnen und Bearbeiten von Tex-Dateien verwendet werden.

## LATEX-Dateiformat

LATEX-Dateien sind einfache Textdateien, die in jedem Texteditor bearbeitet werden können. Das Tex-Schriftsatzsystem wird in der Wissenschaft häufig verwendet, insbesondere in den Bereichen Mathematik, Informatik, Wirtschaft, Ingenieurwesen und ähnlichen anderen. Es besteht aus einer Reihe von Befehlen, die üblicherweise mit einem umgekehrten Schrägstrich beginnen und mit geschweiften Klammern gruppiert sind. Kommentare in einer Tex-Datei beginnen und enden mit doppelten Prozentzeichen (%%).

### LATEX-Beispiel

Der folgende Inhalt kann in eine Textdatei eingefügt werden, um ein einfaches LaTex-Dokument zu erstellen.

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

Die Ausgabe der obigen Befehlsdatei sollte wie folgt aussehen:

{{< figure src="../latex-example.png" alt="Latex-Dateiformat" >}}

## Verweise ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)
* [Latex](http://mally.stanford.edu/~sr/computing/latex-example.html)

