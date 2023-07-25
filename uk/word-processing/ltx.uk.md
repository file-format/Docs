{
  "date" : "2019-10-11",
  "keywords" :[ "файл ltx", "формат файлу ltx", "що таке файл ltx", "файл", "приклад ltx", "розширення файлу ltx", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - Latex Document File",
  "description":"Дізнайтеся про формат файлу LTX та API, які можуть створювати та відкривати файли LTX.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Що таке файл LTX?

Запис із розширенням .ltx — це документ на мові розмітки на основі книги, створений за допомогою верстки, відомої як LaTex. У значній частині випадків він використовується для характеристики верстки розсилок, листів, книг та інших порівняльних записів у різних областях. Latex record design доповнює звіт, використовуючи специфічні розрахунки, замовлення на оформлення архіву та найдрібніші тонкощі. Латексні процесори, наприклад TeXworks, Texmaker, LaTeX Editor, proTeXt і Notepad++, можна використовувати для відкриття та зміни записів Tex.

## Формат файлу LTX

Документи LATEX — це звичайні текстові записи, які можна змінити в будь-якому текстовому процесорі. Структура верстки Tex зазвичай використовується в науковій спільноті, зокрема в сферах математики, розробки програмного забезпечення, фінансових аспектів, дизайну тощо. Він містить групу команд, які зазвичай починаються з похилої пунктуаційної лінії (/uk/) і зібрані хвилястими опорами. Зауваження/коментарі у файлі LTX починаються та закінчуються подвійним відсотком зображень (%%). Файли LTX схожі на файли [.tex](/uk/page-description-language/tex/) і [.latex](/uk/word-processing/latex/), і ви часто знайдете латексні документи, збережені в цих форматах.

### Приклад LTX

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
