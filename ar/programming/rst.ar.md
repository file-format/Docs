{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف RST- ملف reStructuredText" ,
  "description":"تعرف على تنسيق ملف RST وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات RST وفتحها." ,
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2022-04-11"
}

## ما هو ملف RST؟

ملف RST هو تنسيق ملف توثيق فني ، يستخدم بشكل أساسي في مجتمع برمجة Python. إنه ملف نصي مكتوب بلغة الترميز reStructuredText التي تطبق الأنماط والتنسيق على مستندات النص العادي لإنشاء الوثائق. تستخدم ملفات RST التعليقات والمعلومات الأخرى في كود برامج Python لإنشاء وثائق فنية للتطبيق. ومع ذلك ، يمكن أن تحتوي أيضًا على نص يمكن تحويله إلى صفحات ويب بسيطة و [كتب إلكترونية] (/ar/ كتاب إلكتروني /). يمكن استخدام برامج تحرير النصوص مثل Github Atom و GNU Emacs (عبر النظام الأساسي) و Microsoft Notepad (Windows) و Apple TextEdit (Mac) و Vim (Linux) لفتح ملفات RST.

## تنسيق ملف RST

تحتوي ملفات RST على تعليمات برمجية مكتوبة بلغة ترميز reStructuredText. إنه جزء من مشروع Docutils الخاص بـ Python Doc-SIG (مجموعة المصالح الخاصة للتوثيق) الذي يوفر مجموعة من الأدوات لبايثون على غرار Javadoc لجافا. المحلل اللغوي لملف RST foramt مضمن في Docutils ويمكنه استخراج المعلومات من برامج Python لتنسيقها في وثائق البرنامج.

### reStructuredText مثال RST

لنأخذ مثالاً على نص مكتوب بتنسيق ملف RST على النحو التالي.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

عندما يتم إدخال هذا النص إلى معالج rST مثل Docutils ، يكون الإخراج على النحو التالي.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## المرجعي ##

* [reStructuredText - بواسطة Wikipedia] (https://en.wikipedia.org/wiki/ReStructuredText)

