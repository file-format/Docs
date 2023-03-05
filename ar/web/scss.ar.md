---
date: 2019-10-11
keywords: scss , .scss , تنسيق ملف scss , كيفية فتح ملفات scss , ورقة أنماط رائعة نحويًا , معالج css المسبق , sass
مؤلف:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: تنسيق ملف SCSS - ورقة أنماط متتالية
linktitle: SCSS
description: "تعرف على تنسيق ملف SCSS وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات SCSS وفتحها."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## ما هو ملف SCSS؟ ##

SCSS هي الصيغة الثانية لـ Sass (ورقة أنماط رائعة نحويًا) تستخدم الأقواس بدلاً من المسافات البادئة. تم تصميم SCSS بطريقة تجعل ملف CSS3 صالحًا أيضًا ملف SCSS صالحًا. يتم تخزين ملفات SCSS بامتداد .scss.

## لماذا استخدام SCSS ##

نظرًا لأن تصميمات مواقع الويب أصبحت معقدة مما أدى إلى ظهور ملفات [CSS](/ar/ web / css /) كبيرة. يصعب الحفاظ على مثل هذه الملفات. هذا هو المكان الذي يأتي فيه SCSS. تقدم SCSS المتغيرات ، والتداخل ، والمزج ، والواردات ، ووراثة المحدد في تطوير CSS. هذه الإضافات تجعل العمل مع التصميم أكثر متعة.

## كيفية استخدام ملفات SCSS ##

لا يتم تضمين ملفات SCSS مباشرة في مستند [HTML](/ar/ web / html /) مثل CSS. بدلاً من ذلك ، يتم تحويل ملفات SCSS إلى ملفات CSS مضمنة في ملفات HTML. لتثبيت SCSS على نظامك ، اتبع التعليمات الواردة على [Official Sass Site](https://sass-lang.com/install).
لتحويل SCSS إلى CSS ، يمكنك إما تحويل ملف SCSS محفوظ بالفعل أو مشاهدة التغييرات والتحويل عند حفظ الملف. يتم إعطاء الأوامر لكليهما أدناه.

### تحويل مرة واحدة ###

المعلمة الأولى هي ملف SCSS المصدر والمعلمة الثانية هي ملف CSS الناتج.

```cmd
sass main.scss main.css
```

### انتبه للتغييرات ###

يحتوي الأمر على علامة * watch ** إضافية تحافظ على تشغيل الأمر وبمجرد حفظ ملف SCSS ، يتم إنشاء الإخراج CSS.

```cmd
sass --watch main.scss main.css
```

## ## SCSS Syntax ##

يدعم SCSS المتغيرات ، والتداخل ، والمزج ، والواردات ، وراثة المحدد ، وما إلى ذلك. فيما يلي أمثلة على هذه الميزات.

### المتغيرات ###

باستخدام المتغيرات ، يمكنك تعيين معلومات قابلة لإعادة الاستخدام مثل اللون الأساسي أو لون الخلفية لزر الحفظ. يعد هذا مفيدًا إذا كنت بحاجة إلى تغيير تلك المعلومات ، فما عليك سوى تغييرها في مكان واحد ويتم تحديثها أينما يتم استخدامها.

** SCSS **

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

** تم إنشاء CSS **

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### التعشيش ###

يمكنك دمج محددات CSS بشكل مشابه للتسلسل الهرمي لـ HTML. في المثال الموضح أدناه ، يتم تداخل الامتداد داخل كتلة h1.

** SCSS **

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

** تم إنشاء CSS **

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### الخلطات ###

يمكن استخدام Mixins لتجميع الخصائص المتشابهة معًا والتي يتم استخدامها معًا في أماكن متعددة. يمكنك أيضًا تمرير المعلمات إلى mixins.

** SCSS **

** إعلان الخلط **

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

** باستخدام mixin **

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
```

** تم إنشاء CSS **

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### تمديد ###

يعد التمديد / الوراثة مفيدًا في الحالات التي تحتاج فيها خصائص أحد المحددات إلى المشاركة مع محدد آخر. في المثال أدناه ، يأخذ المحدد * .error-not * جميع خصائص * .error-text * selector ويضيف خصائص الحدود والحشو.

** SCSS **

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
```

** تم إنشاء CSS **

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### يستورد ###

يمكن أن يكون الاستيراد مفيدًا في فصل الاهتمامات. يمكنك تقسيم الأنماط بحيث تكون أنماط الرأس في ملف منفصل ، وتكون أنماط التذييل في ملف منفصل ، ويمكن أن تكون جميع متغيرات الألوان المستخدمة في الأنماط في ملف منفصل ، وما إلى ذلك باستخدام هذه التقنية ، تظل الأنماط منظمة. ما عليك سوى استيراد الملفات في ملف SCSS الرئيسي كما هو موضح في المثال أدناه. لا تحتاج إلى تحديد امتداد الملف في تعليمات الاستيراد. يجمع Sass جميع ملفات SCSS مباشرةً. لتجنب استيراد الملفات ليتم تجميعها بشكل مباشر ، يمكنك جعلها جزئية عن طريق إضافة شرطة سفلية (_) قبل اسمها. يمكنك استيراد أجزاء مشابهة لملفات SCSS العادية بدون الشرطة السفلية.

** SCSS **

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

سيكون لمخرج CSS الأنماط من جميع الملفات المستوردة.

## مراجع ##

- [SCSS - ويكيبيديا](https://en.wikipedia.org/wiki/Sass_ (stylesheet_language))
- [ساس](https://sass-lang.com/)

