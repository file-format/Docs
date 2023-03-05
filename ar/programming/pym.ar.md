---
date: 2022-05-09
مؤلف:
  display_name: Kashif Iqbal
draft: false
toc: true
title: تنسيق ملف PYM - ملف المعالج الأولي لماكرو PYM
linktitle: PYM
description: "تعرف على تنسيق ملف PYM وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PYM وفتحها."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## ما هو ملف PYM؟

ملف PYM هو ملف معالج أولي للماكرو يعتمد على لغة برمجة Python. تم تطويره بواسطة VRVis Research وتخزين اختصارات الماكرو. عندما يتم تفسير ملف PYM من خلال مرحلة المعالجة المسبقة لمترجم Python ، يتم توسيع هذه الاختصارات كبدائل لنصها الكامل. بالإضافة إلى ذلك ، فإن العملية الثالثة الاختيارية التي يمكن أن يقوم بها معالج أولي للماكرو هي تضمين الملف. يمكن فتح ملفات PYM في برامج تحرير النصوص مثل Notepad و Notepad ++ و Apple TextEdit و VI على Linux.

## تنسيق ملف PYM

يتم حفظ ملفات PYM كملفات نصية عادية على القرص. يمكن أن يتضمن ملف PYM أيضًا ملفات أخرى باستخدام التوجيه `# include`.

### صيغة PYM

يتم تضمين عبارات PYM بين علامات "" #begin python و "#end python" كما هو موضح أدناه.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### توسعة PYM الماكرو

يتم تمثيل توسع الماكرو PYM من خلال تسلسلين مثل <[و]>. هذه علامات html خاصة ويمكن أن تظهر في أي مكان في السطر. مثال صغير على PYM على النحو التالي.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

ناتج تشغيل هذا من خلال PYM هو كما يلي:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## مراجع ##

* [PYM - معالج أولي ماكرو يعتمد على Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [PYM Interpreters](https://github.com/interpreters/pym)

