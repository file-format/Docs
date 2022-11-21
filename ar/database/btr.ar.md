{
  "date" : "2021-09-06",
  "keywords" :["btr" , "extension" , "ملف" , "تنسيق الملف" , "نوع ملف قاعدة البيانات" , "تنسيق ملف قاعدة البيانات" , "قاعدة بيانات Btrieve"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف BTR وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات BTR وفتحها." ,
  "title" :"BTR - ملف قاعدة بيانات Btrieve" ,
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
} ,
  "lastmod" : "2021-09-06"
}

## ما هو ملف BTR؟

الملف بامتداد .btr هو ملف قاعدة بيانات تم إنشاؤه بواسطة [Btrieve] (https://www.actian.com/) تطبيق قاعدة بيانات المعاملات. على عكس أنظمة إدارة قواعد البيانات العلائقية (RBMS) ، يعتمد Btrieve على طريقة الوصول التسلسلي المفهرس (ISAM) ، وهي طريقة لتخزين البيانات للاسترجاع السريع. يخزن ملف BTR مجموعة من السجلات ويستخدم لإنشاء تقارير حسب المتطلبات. يمكن فتح ملفات BTR باستخدام Pervasive Btrieve Database Manager و Pervasive PSQL Maintenance Utility و Legend Software BTRIEVE Viewer.

## هيكل ملف BTR - مزيد من المعلومات

هيكل البيانات الداخلية ومحاذاة كل بايت في بنية ملف BTR غير متاح للجمهور. ومع ذلك ، Btrieve
يوفر [Btrieve API] (https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi٪2Fbtrintro.htm) التي يمكن استخدامها لقراءة المعلومات من ملفات BTR. وهو متوافق مع لغات البرمجة وبيئات التطوير التالية.

* Embarcadero C / C ++
* إمباركاديرو دلفي
* جنو سي / سي ++
* التركيز الدقيق COBOL
* مايكروسوفت فيجوال بيسك
* Microsoft Visual C ++
* Watcom C / C ++

استرداد البيانات من ملف BTR يعتمد على ملف DDF المرتبط به. بدون DDF ، لن يكون من السهل استرداد المعلومات من مثل هذا الملف.

## مراجع

* [Btrieve - Wikipedia] (https://en.wikipedia.org/wiki/Btrieve)
* [مقدمة إلى Btreive APIs] (https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi٪2Fbtrintro.htm)

