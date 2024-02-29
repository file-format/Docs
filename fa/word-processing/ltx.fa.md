{
  "date": "2019-10-11",
  "keywords": [
"فایل ltx",
"فرمت فایل ltx",
"فایل ltx چیست",
"فایل",
"مثال ltx",
"پسوند فایل ltx",
"افزونه",
"قالب"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "LTX - فایل سند لاتکس",
  "description": "درباره فرمت فایل LTX و APIهایی که می‌توانند فایل‌های LTX را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "LTX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-lt-fax"
}
}،
  "lastmod": "2021-05-18"
}

## فایل LTX چیست؟

یک رکورد با پسوند ltx. یک سند زبان نشانه گذاری مبتنی بر کتاب است که با چارچوب حروفچینی معروف به LaTex ساخته شده است. در بخش بزرگی از موارد، از آن برای توصیف حروفچینی برای توزیع ها، حروف، کتاب ها و سایر ضبط های مقایسه ای در زمینه های مختلف استفاده می شود. طراحی رکورد لاتکس با استفاده از محاسبات خاص، سفارشات برای ترتیب آرشیو و کوچکترین ظرافت ها، گزارش را ارتقا می دهد. پردازنده های لاتکس، به عنوان مثال، TeXworks، Texmaker، LaTeX Editor، proTeXt، و Notepad++ می توانند برای باز کردن و تغییر رکوردهای Tex استفاده شوند.

## فرمت فایل LTX

LATEX documents are plain text records that can be altered in any word processor. Tex typesetting framework is generally utilized in scholarly community particularly in the fields of math, software engineering, financial aspects, designing, and likewise others. It contains a bunch of commands normally beginning with an oblique punctuation line (/) and gathered with wavy supports. Remarks/comments in an LTX file start and end with twofold percent images (%%). LTX files are similar to [.tex](/page-description-language/tex/) and [.latex](/word-processing/latex/) file and you will often find latex documents saved in these formats.

### مثال LTX

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


