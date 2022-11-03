{
  "date" : "2019-10-11",
  "keywords" :[ "файл ltx", "формат файла ltx", "что такое файл ltx", "файл", "пример ltx", "расширение файла ltx", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX — файл латексного документа",
  "description":"Узнайте о формате файла LTX и API-интерфейсах, которые могут создавать и открывать файлы LTX.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## .LTX вариант №

Запись с расширением .ltx представляет собой документ на языке разметки на основе книги, созданный с помощью платформы набора текста, известной как LaTex. В большинстве случаев он используется для характеристики наборов для раздач, писем, книг и других сравнительных записей в различных областях. Латексный дизайн записи обновляет отчет, используя специфические расчеты, порядок оформления архива и мельчайшие тонкости. Для открытия и изменения записей Tex можно использовать процессоры Latex, например TeXworks, Texmaker, LaTeX Editor, proTeXt и Notepad++.

## Формат файла LTX

Документы LATEX представляют собой простые текстовые записи, которые можно изменить в любом текстовом процессоре. Структура набора текста Tex обычно используется в научном сообществе, особенно в области математики, разработки программного обеспечения, финансовых аспектов, проектирования и других. Он содержит набор команд, обычно начинающихся с косой линии препинания (/ru/) и собранных волнистыми опорами. Примечания/комментарии в файле LTX начинаются и заканчиваются изображениями с двойным процентом (%%). Файлы LTX аналогичны файлам [.tex](/ru/page-description-language/tex/) и [.latex](/ru/word-processing/latex/), и вы часто найдете латексные документы, сохраненные в этих форматах.

### Пример LTX

Следующее содержимое можно вставить в текстовый файл для создания простого документа LaTex.

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

Вывод командного файла выше должен выглядеть так:

{{< figure src="../latex-example.png" alt="Латексный формат файла" >}}

## Использованная литература ##

* [TEX - Википедия](https://en.wikipedia.org/wiki/TeX)
* [Латекс](http://mally.stanford.edu/~sr/computing/latex-example.html)

