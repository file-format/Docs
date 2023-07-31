{
  "date" : "2019-10-11",
  "keywords" :["cshtml" , "ملف cshtml" , "تنسيق ملف cshtml" , "نوع ملف cshtml" , "ملف" , "النوع" , "ما هو ملف cshtml"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - صفحة ويب ASP.NET Razor" ,
  "description":"تعرف على تنسيق ملف CSHTML وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CSHTML وفتحها." ,
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-04-29"
}

## ما هو ملف CSHTML؟

الملف بامتداد .cshtml هو ملف HTML [C #](/ar/programming/cs/) يتم استخدامه على جانب الخادم بواسطة محرك Razor Markup لعرض ملفات صفحة الويب إلى متصفح المستخدم. هذا الترميز من جانب الخادم مشابه لصفحة ASP.NET القياسية التي تتيح إنشاء محتوى ويب ديناميكي سريعًا حيث تتم كتابة صفحة الويب في المستعرض. ينفذ الخادم الكود من جانب الخادم داخل الصفحة قبل إرسال الصفحة التي تم إنشاؤها إلى المتصفح. المهام المعقدة مثل الوصول إلى قواعد البيانات وتقديم طرق عرض معقدة. يمكن إنشاء ملفات CSHTML وبرمجتها باستخدام Microsoft Visual Studio.

## تنسيق ملف CSHTML

ملفات CSHTML هي ملفات نصية تتبع بناء الجملة المحدد بواسطة محرك ترميز Razor. يدعم Razor كلاً من C # و VB.NET ، وهو سهل التعلم والاستخدام مقارنة بـ ASP و ASP.NET الكلاسيكيين. تحتوي w3schools على دليل بسيط ولكنه فعال [بناء جملة C # و VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) لترميز Razor.

### مثال CSHTML

فيما يلي مثال C # Code المستخدم في ملف CSHTML لـ Razor.

```
<!-- Single statement block -->
@{ var myMessage = "Hello World"; }

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@{
var greeting = "Welcome to our site!";
var weekDay = DateTime.Now.DayOfWeek;
var greetingMessage = greeting + " Here in Huston it is: " + weekDay;
}
<p>The greeting is: @greetingMessage</p>
```

كود VB.NET المكافئ لـ Razor هو كما يلي.

```
<!-- Single statement block  -->
@Code dim myMessage = "Hello World" End Code

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@Code
dim greeting = "Welcome to our site!"
dim weekDay = DateTime.Now.DayOfWeek
dim greetingMessage = greeting & " Here in Huston it is: " & weekDay
End Code

<p>The greeting is: @greetingMessage</p>
```

## مراجع

* [مرجع بنية الشفرة - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor؟view=aspnetcore-5.0)

