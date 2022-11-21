{
  "date" : "2019-12-12",
  "keywords" :["KF8", "extension", "file", "format", "eBook", "Kindle File Format", "AZW3 File Structure"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف AZW3 وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات AZW3 وفتحها." ,
  "title" :"ما هو ملف AZW3؟" ,
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
} ,
  "lastmod" : "2021-06-04"
}

## ما هو ملف AZW3؟

AZW3 ، المعروف أيضًا باسم Kindle Format 8 (** KF8 **) ، هو الإصدار المعدل من تنسيق الملف الرقمي للكتب الإلكترونية [AZW] (/ar/ ebook / azw /) الذي تم تطويره لأجهزة Amazon Kindle. يعد التنسيق تحسينًا لملفات AZW الأقدم ولا يتم استخدامه على أجهزة Kindle Fire إلا مع التوافق مع الإصدارات السابقة لتنسيق ملف السلف مثل [MOBI] (/ar/ ebook / mobi /) و AZW. قدمت أمازون تنسيق KFX (KF الإصدار 10) بعد KF8 الذي يتم استخدامه على أحدث أجهزة Kindle. تحتوي ملفات AZW3 على تطبيق نوع وسائط الإنترنت / vnd.amazon.mobi8-ebook. يمكن تحويل ملفات AZW3 إلى عدد من تنسيقات الملفات الأخرى مثل [PDF] (/ar/ pdf /) ، [EPUB] (/ar/ ebook / epub /) ، [AZW] (/ar/ ebook / azw /) ، [DOCX] (/ar/ معالجة الكلمات / docx /) و [RTF] (/ar/ معالجة الكلمات / rtf /).

## تنسيق ملف AZ3 / KF8 ##

ملفات KF8 ثنائية بطبيعتها وتحتفظ بهيكل تنسيق ملف MOBI كملف PDB. كما ذكرنا سابقًا ، قد يتكون ملف KF8 من MOBI بالإضافة إلى إصدار KF8 الأحدث من EPUB لاحقًا. تم فك تشفير التفاصيل الداخلية للتنسيق بواسطة [Kindle Unpack] (https://github.com/kevinhendricks/KindleUnpack) ، وهو نص برمجي Python يحلل قاعدة البيانات المجمعة النهائية ويستخرج ملفات MOBI أو AZW المصدر منها. تستهدف ملفات AZW3 (KF8) إصدار EPUB3 مع التوافق مع الإصدارات السابقة لـ EPUB أيضًا. يقوم KF8 بتجميع ملفات EPUB وإنشاء بنية ثنائية بناءً على تنسيق ملف PDB.

## مراجع ##

* [KF8 - بواسطة ويكيبيديا] (https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack] (https://github.com/kevinhendricks/KindleUnpack)

