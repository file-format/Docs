{
  "date" : "2019-10-11",
  "keywords" :["ملف لاتكس" , "تنسيق ملف لاتكس" , "ما هو ملف لاتكس" , "ملف" , "مثال لاتكس" , "امتداد ملف لاتكس" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - ملف مستند لاتكس" ,
  "description":"تعرف على تنسيق ملف LATEX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات LATEX وفتحها." ,
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
} ,
  "lastmod" : "2021-05-18"
}

## ما هو ملف لاتكس؟

الملف بامتداد .latex هو ملف لغة ترميز يستند إلى نص تم إنشاؤه باستخدام نظام التنضيد المعروف باسم LaTex. في معظم الحالات ، يتم استخدامه لتحديد تنضيد المطبوعات والرسائل والكتب والفهرسة المماثلة الأخرى في مختلف المجالات. يعمل تنسيق ملف Latex على تحسين المستند باستخدام خوارزميات متخصصة وأوامر لتنسيق المستند وأدق التفاصيل. يمكن استخدام معالجات Latex مثل TeXworks و Texmaker و LaTeX Editor و proTeXt و Notepad ++ لفتح ملفات Tex وتحريرها.

## تنسيق ملف لاتكس

ملفات LATEX هي ملفات نصية عادية يمكن تحريرها في أي محرر نصوص. يستخدم نظام تنضيد تكس على نطاق واسع في الأوساط الأكاديمية خاصة في مجالات الرياضيات وعلوم الكمبيوتر والاقتصاد والهندسة وغيرها من المجالات المماثلة. وهو يتألف من مجموعة من الأوامر التي تبدأ عادةً بشرطة مائلة للخلف ومجمعة بأقواس متعرجة. تبدأ التعليقات في ملف tex وتنتهي برموز النسبة المئوية المزدوجة (٪٪).

### مثال لاتكس

يمكن لصق المحتوى التالي في ملف نصي لإنشاء مستند LaTex بسيط.

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

يجب أن يبدو إخراج ملف الأوامر أعلاه كما يلي:

{{< figure src="../latex-example.png" alt="تنسيق ملف اللاتكس" >}}

## مراجع ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)

