{
  "date" : "2019-10-11",
  "keywords" :[ "латексный файл", "латексный формат файла", "что такое латексный файл", "файл", "пример латекса", "расширение латексного файла", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX — файл документа латекса",
  "description":"Узнайте о формате файлов LATEX и API, которые могут создавать и открывать файлы LATEX.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## .LATEX вариант №

Файл с расширением .latex представляет собой текстовый файл языка разметки, созданный с помощью системы набора текста, известной как LaTex. В большинстве случаев он используется для определения верстки публикаций, писем, книг и другой подобной каталогизации в различных областях. Формат файла Latex расширяет документ с помощью специализированных алгоритмов, команд форматирования документа и мельчайших деталей. Для открытия и редактирования файлов Tex можно использовать процессоры Latex, такие как TeXworks, Texmaker, LaTeX Editor, proTeXt и Notepad++.

## Формат файла LATEX

Файлы LATEX представляют собой обычные текстовые файлы, которые можно редактировать в любом текстовом редакторе. Система набора текстов широко используется в академических кругах, особенно в области математики, информатики, экономики, инженерии и других подобных областях. Он состоит из набора команд, обычно начинающихся с обратной косой черты и сгруппированных фигурными скобками. Комментарии в текстовом файле начинаются и заканчиваются символами двойного процента (%%).

### Пример ЛАТЕКСа

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
