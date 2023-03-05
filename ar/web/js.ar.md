---
date: 2019-10-11
keywords: js , .js , تنسيق ملف js , كيفية فتح ملفات js , ملفات جافا سكريبت
مؤلف:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: تنسيق ملف JS
linktitle: JS
description: "تعرف على تنسيق ملف JS وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات JS وفتحها."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## ما هو ملف JS؟ ##

JS (JavaScript) هي ملفات تحتوي على كود JavaScript للتنفيذ على صفحات الويب. يتم تخزين ملفات JavaScript بامتداد .js. داخل مستند [HTML](/ar/ web / html /) ، يمكنك إما تضمين كود JavaScript باستخدام \ <script>\</script> العلامات أو تضمين ملف JS. على غرار ملفات [CSS](/ar/ web / css /) ، يمكن تضمين ملفات JS في مستندات HTML متعددة لإعادة استخدام الكود. يمكن استخدام JavaScript لمعالجة HTML DOM.

## نبذة تاريخية ##

تم شحن JavaScript لأول مرة كجزء من متصفح Navigator في سبتمبر 1995 باسم LiveScript بواسطة Netscape. تم تغيير اسمها إلى JavaScript بعد ثلاثة أشهر. في عام 1996 ، قامت Microsoft بإجراء هندسة عكسية لمترجم Navigator لإنشاء JScript. تم إصدار JScript باستخدام Internet Explorer وكان مختلفًا تمامًا عن JavaScript.

قدمت Netscape JavaScript إلى ECMA International مما أدى إلى الإصدار الرسمي لأول مواصفات ECMAScript في عام 1997. تم إصدار ECMAScript 2 في عام 1998 ، و ECMAScript 3 في عام 1999 ، وبدأ العمل على ECMAScript 4 في عام 2000 ولكن لم يتم تحقيقه.

أصدر جيسي جيمس جاريت في عام 2005 ورقة بيضاء حيث صاغ مصطلح * أياكس *. استخدم هذا جافا سكريبت باعتباره العمود الفقري لإنشاء تطبيقات الويب التي حملت البيانات في الخلفية وتجنب إعادة تحميل الصفحة الكاملة. أدى ذلك إلى إنشاء مكتبات مثل JQuery و Prototype و Dojo وما إلى ذلك.

أطلقت Google متصفح Chrome مع محرك جافا سكريبت V8 في عام 2008. في أوائل عام 2009 ، تم الاتفاق على دمج جميع الأعمال ذات الصلة ودفع جافا سكريبت إلى الأمام. أدى ذلك إلى إصدار معيار ECMAScript 5 في ديسمبر 2009.

## كيفية استخدام ملفات JS ##

لاستخدام ملف JS ، عليك تضمينه في مستند HTML. يمكنك استخدام علامة الارتباط لتضمين الملف كما هو موضح أدناه.

```html
<script src="site.js"></script>
```

تحتوي السمة * src * للعلامة * script * على المسار إلى ملف JS. من خلال القيام بذلك ، تتم إضافة وظيفة JS إلى مستند HTML.

## صيغة JS ##

يمكن أن تحتوي ملفات جافا سكريبت على متغيرات ، عوامل تشغيل ، وظائف ، شروط ، حلقات ، مصفوفات ، كائنات ، إلخ. فيما يلي نظرة عامة مختصرة عن بناء جملة JavaScript.

- ينتهي كل أمر بفاصلة منقوطة (؛).
- استخدم الكلمة الأساسية * var * للإعلان عن المتغيرات.
- يدعم العمليات الحسابية (+ - * /) لحساب القيم.
- تمت إضافة تعليقات سطر واحد مع // والتعليقات متعددة الأسطر محاطة بـ / * و * /.
- جميع المعرفات حساسة لحالة الأحرف ، أي * modelNo * و * modelno * هما متغيرين مختلفين.
- يتم تحديد الوظائف باستخدام الكلمة الأساسية * وظيفة *.
- يمكن تعريف المصفوفات باستخدام الأقواس المربعة [].
- يدعم JS عوامل المقارنة مثل == ،! = ،> = ،! == ، إلخ.
- يمكن تعريف الفئات باستخدام الكلمة الأساسية * class *.

## مثال على استخدام JS ##

يوضح ما يلي مثال استخدام بسيط لملف JavaScript.

### مستند HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### كود JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## مراجع ##

- [JS - ويكيبيديا](https://en.wikipedia.org/wiki/JavaScript)

