---
date: 2019-10-11
keywords: sass , .sass , تنسيق ملف sass , كيفية فتح ملفات sass , ورقة أنماط رائعة نحويًا , معالج css المسبق , sass
مؤلف:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: تنسيق ملف Sass
linktitle: Sass
description: "تعرف على تنسيق ملف Sass وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات Sass وفتحها."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## ما هو ملف SASS؟ ##

Sass (أوراق الأنماط الرائعة من الناحية النحوية) هي لغة برمجة نصية ما قبل المعالجة. يتم تجميعه في [CSS] (/ar/ web / css /) ويتم تخزينه بامتداد .sass. يتكون Sass من بناءين ، الأصل يعتمد على المسافات البادئة التي تستخدم الامتداد .sass و SCSS الأحدث مع تنسيق الكتلة مثل CSS الذي يستخدم الامتداد .scss.

## لماذا تستخدم Sass ##

يعد Sass مفيدًا حقًا في الحفاظ على الأنماط لأنه يوفر العديد من الميزات مثل تقديم المتغيرات والتداخل والمزج والاستيراد ووراثة المحدد التي تجعل العمل مع الأنماط أمرًا ممتعًا.

## كيفية استخدام ملفات SASS ##

لا يتم تضمين ملفات SASS مباشرة في مستند [HTML] (/ar/ web / html /) ولكن يتم تحويلها إلى ملفات CSS المضمنة في ملفات HTML. يجوز لك استبعاد Sass من نظامك باتباع الإرشادات الواردة على [Official Sass Site] (https://sass-lang.com/install).

يمكن تحويل Sass إلى CSS إما عن طريق تحويل ملف SASS محفوظ بالفعل أو بمشاهدة التغييرات والتحويل أثناء حفظ الملف. يتم إعطاء الأوامر لكليهما أدناه.

### تحويل مرة واحدة ###

المعلمة الأولى للأمر هي ملف SASS المصدر والمعلمة الثانية هي ملف CSS الناتج.

```cmd
sass main.sass main.css
```

### انتبه للتغييرات ###

يمكن تشغيل الأمر أعلاه بعلامة * watch * إضافية تحافظ على تشغيل الأمر وبمجرد حفظ ملف Sass ، يتم إنشاء إخراج CSS.

```cmd
sass --watch main.sass main.css
```

## ## تركيب ساس ##

يدعم Sass المتغيرات ، والتداخل ، والمزج ، والواردات ، وراثة المحدد ، وما إلى ذلك ، فيما يلي أمثلة على هذه الميزات.

### المتغيرات ###

يمكن استخدام المتغيرات لتعيين معلومات قابلة لإعادة الاستخدام مثل اللون الأساسي أو المساحة المتروكة للزر. يمكن أن يكون هذا مفيدًا إذا احتجت في المستقبل إلى تغيير تلك المعلومات ، ما عليك سوى تغييرها في مكان واحد ويتم تحديثها في كل مكان.

** ساس **

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

يمكن أن تتداخل محددات CSS بشكل مشابه للتسلسل الهرمي لـ HTML. في المثال التالي ، يتم تداخل الامتداد داخل كتلة h1.

** ساس **

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

يتم استخدام Mixins لتجميع الخصائص المتشابهة معًا والتي يتم استخدامها في أماكن متعددة. كما تدعم Mixins المعلمات.

** ساس **

** إعلان الخلط **

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

** باستخدام mixin **

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

يمكن أن يكون التمديد / الوراثة مفيدًا في الحالات التي تحتاج فيها خصائص أحد المحددات إلى المشاركة مع محدد آخر. في المثال أدناه ، يأخذ المحدد * .error-not * جميع خصائص المحدد * .error-text * ويضيف خصائص الحدود والحشو.

** ساس **

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
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

يمكن أن يكون الاستيراد مفيدًا إذا قمت ببناء الأنماط في ملفات مختلفة بناءً على الوظائف أو أي بنية أخرى تتبعها. يمكنك استيراد كل هذه الملفات في ملف SASS أساسي يتم تحويله لاحقًا إلى CSS. أثناء الاستيراد ، لا تحتاج إلى تحديد امتداد الملف في تعليمات الاستيراد. يجمع Sass جميع ملفات SASS مباشرةً. لتجنب استيراد الملفات ليتم تجميعها بشكل مباشر ، يمكنك جعلها جزئية عن طريق إضافة شرطة سفلية (_) في بداية اسمها. يتم استيراد الأجزاء الجزئية بشكل مشابه لملفات Sass العادية.

** ساس **

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

سيكون لمخرج CSS الأنماط من جميع الملفات المستوردة.

## مراجع ##

- [ساس - ويكيبيديا] (https://en.wikipedia.org/wiki/Sass_ (stylesheet_language))
- [ساس] (https://sass-lang.com/)

