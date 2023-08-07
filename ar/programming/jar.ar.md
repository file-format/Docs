{
  "date" : "2019-10-11",
  "keywords" :["JAR", ".jar", "what is a jar file", "how to open a jar file", "extension", "file", "jar file", "jar file format", ".jar extension "] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - تنسيق ملف أرشيف Java" ,
  "description":"تعرف على تنسيق ملف JAR وواجهات برمجة التطبيقات التي يمكنها إنشاء ملف JAR وفتحه." ,
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2020-09-10"
}

## ما هو ملف JAR؟

الملف ذو الامتداد .jar هو ملف Java Archive يحتوي على العديد من الملفات ذات الصلة بالتطبيقات المختلفة كملف واحد. تم إنشاء تنسيق الملف هذا لتقليل سرعة تحميل تطبيق Java الصغير الذي تم تنزيله في المستعرض عبر معاملة HTTP ، عن طريق تجنب إنشاء اتصالات HTTP متعددة. يمكن أن يحتوي ملف JAR واحد على ملفات فئة Java ([.class](/ar/programming/class/)) و [images](/ar/image/) و [sounds](/ar/audio/). يمكن توقيع العناصر الفردية داخل ملف JAR رقميًا بواسطة مطور التطبيق لمصادقة أصلهم. تُستخدم ملفات JAR بانتظام لإنشاء واجهات برمجة تطبيقات وظيفية تحتوي على وظائف محددة مرتبطة بواجهة برمجة التطبيقات تلك.

## تنسيق ملف JAR

تستند ملفات JAR إلى [تنسيق ملف ZIP](/ar/compression/zip/) الذي يعمل على أرشفة ملفات المحتوى الفردية في ملف واحد. يدعم تنسيق ملف JAR عمليات الضغط ، مما ينتج عنه حجم ملف أصغر للتنزيل وبالتالي تحسين وقت التنزيل. توفر [مواصفات ملف JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) من Oracle تفاصيل كاملة حول المواصفات الداخلية لملفات JAR.

### ملف البيان

عندما يتم إنشاء ملف JAR ، يتم إنشاء ملف بيان بداخله تلقائيًا يحتوي على معلومات البيانات الأولية حول محتويات ملف JAR. يعرض هذا الملف المحتويات التي تم حزمها داخل ملف JAR. يبدو ملف Manifest النموذجي كما يلي والذي يعرض المجلدات والفئات المضمنة في ملف JAR.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### مواصفات البيان

تحدد Oracle مواصفات البيان على النحو التالي.

"ملف-البيان": سطر جديد للقسم الرئيسي \ * قسم فردي

"main-section": version-info newline \ * main-attribute

"معلومات الإصدار": إصدار البيان: رقم الإصدار

"رقم الإصدار": رقم + {. رقم +} *

"main-attribute": (أي سمة رئيسية شرعية) سطر جديد

"قسم فردي": الاسم: قيمة سطر جديد \ * سمة لكل فئة

`سمة-لكل فئة`: (أي سمة لكل شريحة شرعية) سطر جديد

"الخط الجديد": CR LF | LF | CR (لا يتبعه LF)

`digit`: {0-9}

### JAR قابل للتنفيذ

يمكن أن تتكون ملفات JAR أيضًا من تطبيق يمكن تنفيذه بواسطة Java Virtual Machine (JVM) على غرار أي تطبيق آخر على نظام تشغيل Microsoft Windows. في هذه الحالة ، يحتاج JVM إلى معرفة نقطة دخول التطبيق التي هي أي فئة ذات طريقة رئيسية عامة باطلة ثابتة. يحدد ملف البيان هذه الفئة برأس "Main-Class" بالتنسيق التالي:

```
Main-Class: com.example.MyClassName
```



## مراجع

* [نظرة عامة على ملف JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [تنسيق ملف JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

