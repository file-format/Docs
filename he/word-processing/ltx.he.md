{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ ltx", "פורמט קובץ ltx", "מהו קובץ ltx", "קובץ", "דוגמה ltx", "סיומת קובץ ltx","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - קובץ מסמכי לטקס",
  "description":"למד על פורמט קובץ LTX וממשקי API שיכולים ליצור ולפתוח קובצי LTX.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## מהו קובץ LTX?

רשומה עם סיומת .ltx היא מסמך שפת סימון המבוסס על ספר שנעשה עם מסגרת הכתיבה המכונה LaTex. בחלק גדול מהמקרים הוא מנוצל לאפיון הגדרות הדפוס להפצות, מכתבים, ספרים והקלטה השוואתית אחרת בתחומים שונים. עיצוב רשומות לטקס משדרג את הדוח תוך שימוש בחישובים ספציפיים, הזמנות לסידור הארכיון והדקויות הקטנות ביותר. ניתן להשתמש במעבדי לטקס, לדוגמה, TeXworks, Texmaker, LaTeX Editor, proTeXt ו-Notepad++ כדי לפתוח ולשנות רשומות Tex.

## פורמט קובץ LTX

מסמכי LATEX הם רשומות טקסט רגיל שניתן לשנות בכל מעבד תמלילים. מסגרת קביעת טקסט מנוצלת בדרך כלל בקהילה מלומדים במיוחד בתחומי מתמטיקה, הנדסת תוכנה, היבטים פיננסיים, עיצוב, וכמו כן אחרים. הוא מכיל חבורה של פקודות שמתחילות בדרך כלל בשורת פיסוק אלכסונית (/he/) ונאספות עם תומכים גליים. הערות/הערות בקובץ LTX מתחילות ומסתיימות באחוזים כפולים (%%). קבצי LTX דומים לקובץ [.tex](/he/page-description-language/tex/) ו-[.latex](/he/word-processing/latex/) ולעתים קרובות תמצא מסמכי לטקס שנשמרו בפורמטים אלה.

### דוגמה ל-LTX

ניתן להדביק את התוכן הבא בקובץ טקסט כדי ליצור מסמך LaTex פשוט.

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

הפלט של קובץ הפקודה למעלה אמור להיראות כך:

{{< figure src="../latex-example.png" alt="פורמט קובץ לטקס" >}}

## הפניות ##

* [TEX - ויקיפדיה](https://en.wikipedia.org/wiki/TeX)

