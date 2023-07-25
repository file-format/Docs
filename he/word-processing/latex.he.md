{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ לטקס", "פורמט קובץ לטקס", "מהו קובץ לטקס", "קובץ", "דוגמה לטקס", "סיומת קובץ לטקס", "הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - קובץ מסמכי לטקס",
  "description":"למד על פורמט קובץ LATEX וממשקי API שיכולים ליצור ולפתוח קובצי LATEX.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## מהו קובץ LATEX?

קובץ עם סיומת .latex הוא קובץ שפת סימון מבוסס טקסט שנוצר עם מערכת הקביעת הקלדה הידועה בשם LaTex. ברוב המקרים הוא משמש להגדרת הגדרות הדפוס לפרסומים, מכתבים, ספרים ועוד קיטלוג דומה בתחומים שונים. פורמט קובץ לטקס משפר את המסמך באמצעות אלגוריתמים מיוחדים, פקודות לעיצוב המסמך והפרטים הקטנים ביותר. ניתן להשתמש במעבדי לטקס כגון TeXworks, Texmaker, LaTeX Editor, proTeXt ו-Notepad++ כדי לפתוח ולערוך קבצי טקס.

## פורמט קובץ LATEX

קבצי LATEX הם קבצי טקסט רגיל שניתן לערוך בכל עורך טקסט. מערכת קביעת טקסטים נמצאת בשימוש נרחב באקדמיה, במיוחד בתחומי המתמטיקה, מדעי המחשב, כלכלה, הנדסה ובדומה אחרים. הוא מורכב מקבוצה של פקודות שמתחילות בדרך כלל עם נטוי אחורי ומקובצות בסוגריים מסולסלים. הערות בקובץ טקסט מתחילות ומסתיימות בסמלי אחוז כפול (%%).

### LATEX דוגמה

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

