{
  "date" : "2019-10-11",
  "keywords" :[ "латекс файл", "латекс файл формат", "какво е латекс файл", "файл", "латекс пример", "латекс файл разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Латексов файл с документи",
  "description":"Научете за файловия формат LATEX и API, които могат да създават и отварят LATEX файлове.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Какво е LATEX файл?

Файл с разширение .latex е базиран на текст файл с език за маркиране, създаден със системата за набор, известна като LaTex. В повечето случаи се използва за определяне на наборите за публикации, писма, книги и други подобни каталогизации в различни области. Latex файловият формат подобрява документа с помощта на специализирани алгоритми, команди за форматиране на документа и най-малките детайли. Латекс процесори като TeXworks, Texmaker, LaTeX Editor, proTeXt и Notepad++ могат да се използват за отваряне и редактиране на Tex файлове.

## LATEX файлов формат

LATEX файловете са обикновени текстови файлове, които могат да се редактират във всеки текстов редактор. Tex наборната система е широко използвана в академичните среди, особено в областите на математиката, компютърните науки, икономиката, инженерството и подобни други. Състои се от набор от команди, обикновено започващи с обратна наклонена черта и групирани с фигурни скоби. Коментарите в текстов файл започват и завършват с двойни символи за процент (%%).

### Пример за ЛАТЕКС

Следното съдържание може да бъде поставено в текстов файл, за да се създаде прост LaTex документ.

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

Резултатът от командния файл по-горе трябва да изглежда така:

{{< figure src="../latex-example.png" alt="Латексов файлов формат" >}}

## Препратки ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)
* [Латекс](http://mally.stanford.edu/~sr/computing/latex-example.html)

