{
  "date": "2019-10-11",
  "keywords": [
"فایل لاتکس",
"فرمت فایل لاتکس",
"فایل لاتکس چیست",
"فایل",
"نمونه لاتکس",
"پسوند فایل لاتکس",
"افزونه",
"قالب"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "لاتکس - فایل سند لاتکس",
  "description": "درباره فرمت فایل LATEX و APIهایی که می توانند فایل های LATEX را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "LATEX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-late-fax"
}
}،
  "lastmod": "2021-05-18"
}

## فایل لاتکس چیست؟

یک فایل با پسوند latex. یک فایل زبان نشانه گذاری مبتنی بر متن است که با سیستم حروفچینی معروف به LaTex ایجاد شده است. در بیشتر موارد برای تعریف حروفچینی نشریات، نامه ها، کتاب ها و سایر فهرست نویسی های مشابه در زمینه های مختلف استفاده می شود. فرمت فایل لاتکس با استفاده از الگوریتم های تخصصی، دستورات قالب بندی سند و جزییات کوچک، سند را بهبود می بخشد. از پردازنده های لاتکس مانند TeXworks، Texmaker، LaTeX Editor، proTeXt و Notepad++ می توان برای باز کردن و ویرایش فایل های Tex استفاده کرد.

## فرمت فایل لاتکس

فایل های لاتکس فایل های متنی ساده ای هستند که در هر ویرایشگر متنی قابل ویرایش هستند. سیستم حروفچینی متن به طور گسترده در دانشگاه به ویژه در زمینه های ریاضیات، علوم کامپیوتر، اقتصاد، مهندسی و موارد مشابه استفاده می شود. این شامل مجموعه ای از دستورات است که معمولاً با علامت بک اسلش شروع می شود و با بریس های مجعد گروه بندی می شود. نظرات در یک فایل متنی با نمادهای دو درصد (%%) شروع و پایان می‌یابد.

### مثال لاتکس

محتوای زیر را می توان در یک فایل متنی جایگذاری کرد تا یک سند لاتکس ساده ایجاد شود.

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

خروجی فایل فرمان بالا باید به شکل زیر باشد:

{{< figure src="../latex-example.png" alt="فرمت فایل لاتکس" >}}

## منابع ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)


