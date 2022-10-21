{
  "date" : "2019-10-11",
  "keywords" :[ "ltx-Datei", "ltx-Dateiformat", "was ist eine ltx-Datei", "Datei", "ltx-Beispiel", "ltx-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - Latex-Dokumentdatei",
  "description":"Erfahren Sie mehr über das LTX-Dateiformat und APIs, die LTX-Dateien erstellen und öffnen können.",
  "linktitle" :"LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Was ist eine LTX-Datei?

Ein Datensatz mit der Erweiterung .ltx ist ein buchbasiertes Auszeichnungssprachendokument, das mit dem als LaTex bekannten Schriftsatz-Framework erstellt wurde. In einem großen Teil der Fälle wird es verwendet, um die Schriftsätze für Verteilungen, Briefe, Bücher und andere vergleichende Aufzeichnungen in verschiedenen Bereichen zu charakterisieren. Das Latex-Record-Design wertet den Bericht durch spezifische Berechnungen, Ordnungsbefehle für das Archiv und die kleinsten Feinheiten auf. Latex-Prozessoren, zum Beispiel TeXworks, Texmaker, LaTeX Editor, proTeXt und Notepad++, können verwendet werden, um Tex-Datensätze zu öffnen und zu ändern.

## LTX-Dateiformat

LATEX-Dokumente sind einfache Textdatensätze, die in jedem Textverarbeitungsprogramm geändert werden können. Das Textsatz-Framework von Tex wird im Allgemeinen in der wissenschaftlichen Gemeinschaft verwendet, insbesondere in den Bereichen Mathematik, Softwareentwicklung, finanzielle Aspekte, Design und andere. Es enthält eine Reihe von Befehlen, die normalerweise mit einer schrägen Interpunktionslinie (/de/) beginnen und mit wellenförmigen Stützen zusammengefasst sind. Bemerkungen/Kommentare in einer LTX-Datei beginnen und enden mit zweifachen Prozentbildern (%%). LTX-Dateien ähneln [.tex](/de/page-description-language/tex/)- und [.latex](/de/word-processing/latex/)-Dateien, und Sie finden häufig Latexdokumente, die in diesen Formaten gespeichert sind.

### LTX-Beispiel

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

