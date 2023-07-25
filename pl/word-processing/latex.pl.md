{
  "date" : "2019-10-11",
  "keywords" :["plik lateksowy", "format pliku lateksowego", "co to jest plik lateksowy", "plik", "przykład lateksowy", "rozszerzenie pliku lateksowego", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - plik dokumentu lateksowego",
  "description":"Dowiedz się o formacie plików LATEX i interfejsach API, które mogą tworzyć i otwierać pliki LATEX.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Czym jest plik LATEX?

Plik z rozszerzeniem .latex to tekstowy plik języka znaczników utworzony za pomocą systemu składu znanego jako LaTex. W większości przypadków służy do definiowania składu publikacji, listów, książek i innych podobnych katalogów z różnych dziedzin. Format pliku Latex ulepsza dokument za pomocą wyspecjalizowanych algorytmów, poleceń formatowania dokumentu i najdrobniejszych szczegółów. Procesory lateksowe, takie jak TeXworks, Texmaker, LaTeX Editor, proTeXt i Notepad++ mogą być używane do otwierania i edytowania plików Tex.

## Format pliku LATEX

Pliki LATEX to zwykłe pliki tekstowe, które można edytować w dowolnym edytorze tekstu. System składu Tex jest szeroko stosowany w środowisku akademickim, zwłaszcza w dziedzinach matematyki, informatyki, ekonomii, inżynierii i podobnych innych. Składa się z zestawu poleceń zwykle rozpoczynających się ukośnikiem odwrotnym i pogrupowanych w nawiasy klamrowe. Komentarze w pliku tex zaczynają się i kończą symbolami podwójnego procentu (%%).

### LATEX Przykład

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
