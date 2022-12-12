{
  "date" : "2019-10-11",
  "keywords" :["plik ltx", "format pliku ltx", "co to jest plik ltx", "plik", "przykład ltx", "rozszerzenie pliku ltx", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - plik dokumentu lateksowego",
  "description":"Poznaj format plików LTX i interfejsy API, które mogą tworzyć i otwierać pliki LTX.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Czym jest plik LTX?

Rekord z rozszerzeniem .ltx to oparty na książkach dokument języka znaczników utworzony za pomocą struktury składu znanej jako LaTex. W dużej części przypadków służy do scharakteryzowania składu dystrybucji, listów, książek i innych nagrań porównawczych z różnych dziedzin. Projekt płyty lateksowej aktualizuje raport, wykorzystując określone obliczenia, polecenia dotyczące aranżacji archiwum i najdrobniejsze subtelności. Procesory lateksowe, na przykład TeXworks, Texmaker, LaTeX Editor, proTeXt i Notepad++, mogą być wykorzystywane do otwierania i modyfikowania rekordów Tex.

## Format pliku LTX

Dokumenty LATEX to zwykłe rekordy tekstowe, które można modyfikować w dowolnym edytorze tekstu. Struktura składu tekstu jest powszechnie stosowana w społeczności naukowej, szczególnie w dziedzinie matematyki, inżynierii oprogramowania, aspektów finansowych, projektowania i innych. Zawiera kilka poleceń zwykle rozpoczynających się ukośną linią interpunkcyjną (/pl/) i zebranych za pomocą falistych podpór. Uwagi/komentarze w pliku LTX zaczynają się i kończą dwukrotnością obrazów procentowych (%%). Pliki LTX są podobne do plików [.tex](/pl/page-description-language/tex/) i [.latex](/pl/word-processing/latex/) i często można znaleźć dokumenty lateksowe zapisane w tych formatach.

### LTX Przykład

Następującą treść można wkleić do pliku tekstowego, aby utworzyć prosty dokument LaTex.

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

Dane wyjściowe powyższego pliku poleceń powinny wyglądać następująco:

{{< figure src="../latex-example.png" alt="Format pliku lateksowego" >}}

## Bibliografia ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)
* [Latex](http://mally.stanford.edu/~sr/computing/latex-example.html)

