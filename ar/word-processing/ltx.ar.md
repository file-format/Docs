{
  "date" : "2019-10-11",
  "keywords" :["ملف ltx" , "تنسيق ملف ltx" , "ما هو ملف ltx" , "ملف" , "مثال ltx" , "امتداد ملف ltx" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - ملف مستند لاتكس" ,
  "description":"تعرف على تنسيق ملف LTX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات LTX وفتحها." ,
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
} ,
  "lastmod" : "2021-05-18"
}

## ما هو ملف LTX؟

السجل بامتداد .ltx هو مستند لغة ترميز مستند إلى كتاب تم إنشاؤه باستخدام إطار عمل التنضيد المعروف باسم LaTex. في جزء كبير من الحالات ، يتم استخدامه لتوصيف تنضيد التوزيعات والرسائل والكتب والتسجيلات المقارنة الأخرى في مختلف المجالات. يعمل تصميم سجل Latex على ترقية التقرير باستخدام حسابات محددة وأوامر لترتيب الأرشيف وأصغر التفاصيل الدقيقة. يمكن استخدام معالجات Latex ، على سبيل المثال ، TeXworks و Texmaker و LaTeX Editor و proTeXt و Notepad ++ لفتح وتعديل سجلات Tex.

## تنسيق ملف LTX

مستندات LATEX عبارة عن سجلات نصية عادية يمكن تغييرها في أي معالج نصوص. يستخدم إطار عمل التنضيد بشكل عام في المجتمع الأكاديمي خاصة في مجالات الرياضيات وهندسة البرمجيات والجوانب المالية والتصميم وغيرها. يحتوي على مجموعة من الأوامر التي تبدأ عادةً بخط ترقيم مائل (/) ويتم تجميعها باستخدام دعامات متموجة. تبدأ الملاحظات / التعليقات في ملف LTX وتنتهي بنسبة مضاعفة من الصور (٪٪). تشبه ملفات LTX ملفات [.tex](/ar/page-description-language/tex/) و [.latex](/ar/word-processing/latex/) وستجد غالبًا مستندات لاتكس محفوظة بهذه التنسيقات.

### مثال LTX

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

