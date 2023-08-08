{
  "date" : "2021-07-23",
  "keywords" :["PL" , "file" , "extension" , "format" , "Perl" , "لغة Perl" , "ملفات PL" , "برمجة"] ,
  "author" : {
    "display_name" : "Sami Cheema"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف PL وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PL وفتحها." ,
  "title" :"ملف PL - تنسيق ملف Perl Script" ,
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-07-23"
}

## PL ما هو ملف PL؟

الملف ذو الامتداد .pl هو ملف Perl Script وهو لغة برمجة نصية. يتم تجميعها وتشغيلها باستخدام برنامج Perl Interpreter. يحتوي ملف البرنامج النصي PL على سطور من التعليمات البرمجية والمتغيرات والتعليقات. لغات البرمجة النصية صعبة نسبيًا
فهم تنسيقات ملفات البرمجة الأخرى مثل [PHP](/ar/programming/php/). يمكن إنشاء ملفات PL وهي متوافقة مع أنظمة التشغيل Windows و macOS و Linux.

## تاريخ موجز للغة برمجة بيرل

تم الاحتفاظ بهذه اللغة لأول مرة في عام 1987 ، لذلك حصلت هذه الملفات على أصلها في ذلك العام. في عام 1989 تم إصدار Perl 2. في وقت لاحق ، تم تحديثه وتعديله حتى الإصدار 5.35 ، ومن المقرر إطلاق الإصدار التالي في العام المقبل.

في كل تحديث ، تمت إضافة أدوات حول الوظائف والأداء ومظهر اللغة والملفات. كانت هناك العديد من التنقيحات حول الإصدارات في هذه السنوات. كانت في الأصل لغة برمجة نصية أساسية ولكنها الآن تضم العديد من الوحدات النمطية الأخرى أيضًا. في الأصل ، كانت لغة بسيطة للغاية ، لكن نصوص هذه اللغة كان من الصعب جدًا فهمها لأنها كانت مضغوطة.

## مواصفات ملحق تنسيق ملف Perl

هناك بعض الخصائص أو المواصفات لملفات البرمجة هذه ، بعضها كالتالي:

* الشفرة المضمنة في هذه الملفات بتنسيق نص عادي وتستخدم لتطوير البرنامج النصي
* البرمجة النصية للخادم ، وتحليل النص ، وإدارة الخادم هي الجوانب الرئيسية التي يغطيها نص هذه اللغة
* العديد من البرامج الشائعة المرتبطة بهذه اللغة هي Active state Active Perl و Bare Bones BBEdit (متوافق مع نظام التشغيل Mac OS)
* تعتبر هذه اللغة لغة عالية المستوى
* بالنسبة لـ Win32 ، قد يضطر المستخدم إلى تثبيت التوزيع الثنائي الأصلي للغة
* تتطلب بعض أدوات البرمجة النصية لتصبح قابلة للتنفيذ في مجموعات موارد Windows المختلفة
* Visual Studio .NET هو إطار عمل مشهور لتطوير لغات البرمجة. تُستخدم أداة Active State المعروفة باسم Visual Perl لإضافة Perl إلى Visual studio
* في الملفات ، يصف السطر الأول من شفرة المصدر معلومات المترجم الفوري المستخدم. تبدأ ملفات PL عادةً بالسطر ** #! / usr / bin / perl ** الذي يخبر جهاز الكمبيوتر الخاص بك بتشغيل هذا البرنامج النصي باستخدام مترجم Perl مثبت في الكمبيوتر


## أمثلة على البرنامج النصي PL

```
#!/usr/bin/perl
print "Hello, world\n";
```

هذا سوف يطبع

```
Hello, World
```

### تعليق سطر واحد ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### تعليق متعدد الأسطر ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### مهمة متغيرة ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### تخصيص المتغير القياسي ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### عمليات عددية بسيطة ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## مراجع ##

- [Python (لغة برمجة) - ويكيبيديا](https://en.wikipedia.org/wiki/Python_(programming_language))

