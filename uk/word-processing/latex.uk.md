{
  "date" : "2019-10-11",
  "keywords" :[ "файл латексу", "формат файлу латексу", "що таке файл латексу", "файл", "приклад латексу", "розширення файлу латексу", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - файл латексного документа",
  "description":"Дізнайтеся про формат файлів LATEX та API, які можуть створювати та відкривати файли LATEX.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Що таке файл LATEX?

Файл із розширенням .latex — це текстовий файл мови розмітки, створений за допомогою системи верстки, відомої як LaTex. У більшості випадків він використовується для визначення набору для публікацій, листів, книг та іншої подібної каталогізації в різних галузях. Формат латексного файлу покращує документ за допомогою спеціальних алгоритмів, команд для форматування документа та найдрібніших деталей. Латексні процесори, такі як TeXworks, Texmaker, LaTeX Editor, proTeXt і Notepad++, можна використовувати для відкриття та редагування файлів Tex.

## Формат файлу LATEX

Файли LATEX — це звичайні текстові файли, які можна редагувати в будь-якому текстовому редакторі. Система верстки Tex широко використовується в наукових колах, особливо в галузях математики, інформатики, економіки, інженерії тощо. Він складається з набору команд, які зазвичай починаються зі зворотної косої риски та згруповані фігурними дужками. Коментарі в текстовому файлі починаються і закінчуються подвійними символами відсотків (%%).

### Приклад LATEX

Наступний вміст можна вставити в текстовий файл, щоб створити простий документ LaTex.

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

Вихід командного файлу вище має виглядати так:

{{< figure src="../latex-example.png" alt="Формат файлу Latex" >}}

## Посилання ##

* [TEX - Вікіпедія](https://en.wikipedia.org/wiki/TeX)
* [Латекс](http://mally.stanford.edu/~sr/computing/latex-example.html)

