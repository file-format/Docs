{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - ملف حزمة المثبت عبر الأنظمة الأساسية" ,
  "description":"تعرف على تنسيق ملف XPI وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات XPI وفتحها." ,
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
} ,
  "lastmod" : "2022-06-07"
}

## ما هو ملف XPI؟

ملف XPI هو أرشيف تثبيت يتم ضغطه لتقليل حجم الملف. يتم استخدامه بواسطة تطبيقات Mozilla لتثبيت المكونات الإضافية والملفات الإضافية. يحتوي على نص تثبيت أو بيان في جذر الملف مع عدد من ملفات البيانات. قد يحتوي ملف XPI على سمات أو مجموعة أدوات أو ملحقات Firefox التي يمكن للمستخدم تثبيتها لتصبح جزءًا من متصفح Firefox أو Thunderbird أو SeaMonkey.

## تنسيق ملف XPI - مزيد من المعلومات

يتم حفظ ملفات XPI على القرص كأرشيفات [ZIP](/ar/compression/zip/) تجمع عدة ملفات في ملف مضغوط واحد. قد تتضمن الملفات الموجودة داخل ملف XPI ملف نصي للتثبيت مثل JS وملفات الويب مثل [CSS](/ar/web/css/) و [HTML](/ar/web/html/) و [JSON](/ar/web/json/). في بعض الأحيان ، قد يحتوي أيضًا على ملفات صور [PNG](/ar/image/png/) لاستخدامها كرموز بواسطة الوظيفة الإضافية.

### كيف يتم عرض محتويات ملف XPI؟

ملف XPI هو عمليا أرشيف مضغوط يمكن عرض محتوياته باستخدام الخطوات التالية.

* تغيير امتداد الملف من XPI إلى ZIP
* استخرج محتويات الملف باستخدام أي أداة مساعدة قياسية لفك الضغط مثل WinZip (Windows ، Mac) ، 7-Zip (Windows) ، أو Apple Archive Utility (Mac).

### قم بتثبيت ملف XPI على Firefox Android

يشعر معظم الناس بالفضول لمعرفة ما إذا كان يمكن تثبيت ملفات XPI في Firefox على أجهزة Android. على نظام Android ، يمكنك تثبيت الوظيفة الإضافية من ملف XPI عن طريق تحديد موقع الملف وفتحه باستخدام Firefox.

## مراجع

* [XPInstall - Wikipedia](https://en.wikipedia.org/wiki/XPInstall)
* [كيف يمكنني فتح امتداد ملف XPI؟](https://support.mozilla.org/en-US/questions/1009049)

