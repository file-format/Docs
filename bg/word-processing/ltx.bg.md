{
  "date" : "2019-10-11",
  "keywords" :[ "ltx файл", "ltx файлов формат", "какво е ltx файл", "файл", "ltx пример", "ltx файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - файл с латексни документи",
  "description":"Научете за LTX файловия формат и API, които могат да създават и отварят LTX файлове.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Какво е LTX файл?

Запис с разширение .ltx е документ на език за маркиране, базиран на книга, направен с рамката за набор, известна като LaTex. В голяма част от случаите се използва за характеризиране на наборите за разпределения, писма, книги и други сравнителни записи в различни области. Дизайнът на латексния запис надгражда отчета чрез специфични изчисления, поръчки за подреждане на архива и най-малките тънкости. Латекс процесори, например, TeXworks, Texmaker, LaTeX Editor, proTeXt и Notepad++ могат да се използват за отваряне и промяна на Tex записи.

## LTX файлов формат

LATEX документите са обикновени текстови записи, които могат да бъдат променяни във всеки текстов процесор. Tex наборната рамка обикновено се използва в научната общност, особено в областта на математиката, софтуерното инженерство, финансовите аспекти, проектирането и други подобни. Той съдържа куп команди, обикновено започващи с наклонена пунктуационна линия (/bg/) и събрани с вълнообразни опори. Забележките/коментарите в LTX файл започват и завършват с двоен процент изображения (%%). LTX файловете са подобни на [.tex](/bg/page-description-language/tex/) и [.latex](/bg/word-processing/latex/) файлове и често ще намерите латексови документи, записани в тези формати.

### Пример за LTX

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

