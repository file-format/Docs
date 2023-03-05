{
  "date" : "2019-10-11",
  "keywords" :["ملف tbz" , "تنسيق ملف tbz" , "ما هو ملف tbz" , "ملف" , "مثال tbz" , "امتداد ملف tbz" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - أرشيف القطران المضغوط Bzip" ,
  "description":"تعرف على تنسيق ملف TBZ وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات TBZ وفتحها." ,
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
} ,
  "lastmod" : "2021-04-05"
}

## ما هو ملف TBZ؟

الملف ذو الامتداد .tbz هو أرشيف مضغوط يستخدم ضغط BZIP لتقليل حجم ملفات المحتوى. ملفات TBZ هي في الواقع ملفات مؤرشفة UNIX [TAR](/ar/ compression / tar /) يتم ضغطها باستخدام BZIP بعد ذلك. أحدث ضغط من المستوى الثاني هو [BZIP2](/ar/ compression / bz2 /) الذي حل محل BZIP. تنسيق ملف TBZ مناسب لنقل الملفات الكبيرة. يمكن فتح / استخراج ملفات TBZ باستخدام تطبيقات برمجية مثل 7-Zip و PeaZip و jZip. يمكن لمستخدمي Linux و macOS أيضًا فتح TBZ باستخدام الأمر BZIP2 من نافذة طرفية.

## تنسيق ملف TBZ

ملفات TBZ هي في الواقع أرشيفات مضغوطة تم إنشاؤها باستخدام ضغط BZIP / [BZIP2](/ar/ compression / bz2). لا توجد مواصفات رسمية متاحة لتنسيق الملف هذا. ومع ذلك ، تشير [المواصفات الهندسية العكسية] غير الرسمية (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) إلى أن دفق .bz2 يتكون من رأس 4 بايت يتبع بمقدار صفر أو أكثر من الكتل المضغوطة.

## مراجع ##

* [مواصفات تنسيق BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

