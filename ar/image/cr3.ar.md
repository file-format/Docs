{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف CR3 - ملف صورة Canon Raw 3" ,
  "description":"تعرف على تنسيق ملف CR3 وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CR3 وفتحها." ,
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
} ,
  "lastmod" : "2022-03-26"
}

## ما هو ملف CR3؟

ملف CR3 هو تنسيق ملف صورة Canon RAW يتم إنشاؤه بواسطة كاميرات رقمية محددة من Canon. تم تقديمه بواسطة Canon ليحل محل تنسيق ملف CR2 ويستخدمه بعض أجهزة Canon الرقمية. تقوم ملفات CR3 بتخزين بيانات الصورة الأصلية غير المفقودة التي لم تتم معالجتها والتي تم التقاطها بواسطة الكاميرا. يوفر استخدام هذه الصور الأولية صورًا عالية الجودة ويتيح مساحة كبيرة لتحرير المصورين. بالإضافة إلى بيانات الصورة الرئيسية ، تخزن ملفات CR3 أيضًا معلومات البيانات الأولية حول الصورة.

## تنسيق ملف CR3

يتم تخزين ملفات CR3 على قرص كملف ثنائي بتنسيق ملف وسائط قاعدة ISO (ISO / IEC 14496-12) ويتضمن أيضًا [علامات Canon] المخصصة (https://exiftool.org/TagNames/Canon.html#uuid). يتضمن أيضًا [برنامج ترميز Canon 'crx](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) وهو مزيج من JPEG-LS (Rice-Golomb + RLE الترميز) و JPEG-2000 (LeGall 5/3 DWT + التقدير الكمي).

## علامات مخصصة CR3

تحتوي ملفات CR3 على علامات مخصصة لأغراض مختلفة. بعض هذه العلامات على النحو التالي.

| معرف العلامة | اسم العلامة | قابل للكتابة | القيم / الملاحظات |
---|---|---|---|
| 'CCTP' | CanonCCTP | - | -> Canon CCTP العلامات |
| 'CMT1' | IFD0 | - | -> علامات EXIF |
| 'CMT2' | ExifIFD | - | -> علامات EXIF |
| 'CMT3' | MakerNoteCanon | - | -> علامات كانون |
| 'CMT4' | معلومات GPS | - | -> علامات GPS |
| 'CNCV' | CompressorVersion | لا | |
| 'CNOP' | CanonCNOP | - | -> كانون CNOP العلامات |
| 'CNTH' | CanonCNTH | - | -> العلامات CNTH من Canon |
| 'THMB' | ThumbnailImage | لا | |

## مراجع

* [تنسيق ملف CR2](http://lclevy.free.fr/cr2/)
* [علامات Canon](https://exiftool.org/TagNames/Canon.html#uuid)

