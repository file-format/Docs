---
date: 2019-10-11
keywords: css , .css , تنسيق ملف css , كيفية فتح ملفات css , أوراق الأنماط المتتالية
مؤلف:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: تنسيق ملف CSS
linktitle: CSS
description: "تعرف على تنسيق ملف CSS وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CSS وفتحها."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## ما هو ملف CSS؟ ##

CSS (أوراق الأنماط المتتالية) هي ملفات تصف كيفية عرض عناصر HTML على الشاشة ، والورق ، وما إلى ذلك. باستخدام HTML ، يمكنك الحصول على أنماط أو أنماط مضمنة يمكن تعريفها في ورقة أنماط خارجية. لتضمين الأنماط ، <style>\</style> العلامات المستخدمة. يتم تخزين أوراق الأنماط الخارجية في ملفات بامتداد .css. باستخدام CSS الخارجي ، يمكنك تضمينه في صفحات HTML متعددة لتحديث نمط تلك الصفحات. يمكن استخدام ملف CSS واحد لتصميم موقع ويب كامل.

## نبذة تاريخية ##

تم إصدار CSS1 في عام 1996 مع بيرت بوس كمؤلف مشارك. بدأت مجموعة عمل CSS العمل على القضايا التي لم يتم تناولها في CSS1. نتج عن ذلك إنشاء CSS2 في نوفمبر 1997 والذي تم نشره كتوصية W3C في 12 مايو 1998. أضاف هذا الإصدار دعمًا للأجهزة الخاصة بالوسائط مثل الطابعات والخطوط القابلة للتنزيل والجداول وتحديد موضع العناصر. في يونيو 1999 ، أصبح CSS3 توصية W3C. أدى ذلك إلى تقسيم الوثائق إلى وحدات نمطية حيث تحتوي كل وحدة على ميزات امتداد محددة في CSS2.

## كيفية استخدام ملفات CSS ##

لاستخدام ملف CSS ، عليك تضمينه في قسم الرأس في مستند HTML. يمكنك استخدام علامة الارتباط لتضمين الملف كما هو موضح أدناه.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

تحتوي السمة * href * لعلامة الارتباط على المسار إلى ملف CSS. من خلال القيام بذلك ، يتم تطبيق الأنماط القابلة للتطبيق الموجودة في ملف CSS المضمن على مستند HTML.

## بنية CSS ##

تتكون قاعدة CSS من مكونين ، محدد وإعلان. محدد يشير إلى عنصر في وثيقة HTML. يمكن أن يكون إما علامة عنصر ، أو اسم فئة ، أو اسم معرف ، أو علامات متعددة توضح التسلسل الهرمي ، وما إلى ذلك. يحتوي الإعلان على تعريف النمط الذي يتكون من الخاصية والقيمة. تحدد الخاصية خاصية العنصر الذي تريد تغييره وتحدد القيمة قيمته الجديدة. يمكن أن تحتوي كل قاعدة CSS على إقرارات متعددة. فيما يلي مثال على قاعدة CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

في المثال أعلاه ، لدينا ** h1 ** كمحدد يحدد جميع علامات h1 في مستند HTML. تحتوي القاعدة على إعلانين ، أحدهما لوزن الخط والآخر للون. * font-weight * و * color * هما خصائص و * 700 * و * forestgreen * هما قيمهما على التوالي.

## مثال على استخدام CSS ##

يعرض ما يلي مثال مستند HTML وورقة الأنماط المستخدمة لتصميمه. تتم إضافة صورة المقارنة أيضًا لمقارنة مستندات HTML ذات الأنماط والعادي

### مستند HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### ورقة أنماط CSS ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### مقارنة المخرجات ###

يعرض الجانب الأيسر من الصورة مستند HTML بدون الأنماط المطبقة ويعرض الجانب الأيمن مستند HTML مع الأنماط المطبقة.

{{< figure src="../CssExample.jpg" alt="مثال على الصورة" >}}

## مراجع ##

- [CSS - ويكيبيديا] (https://en.wikipedia.org/wiki/CSS)

