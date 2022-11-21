{
  "date" : "2021-08-29",
  "keywords" :["ade" , "extension" , "file" , "تنسيق الملف" , "نوع ملف قاعدة البيانات" , "تنسيق ملف قاعدة البيانات" , "Microsoft Access"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف ADE وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات ADE وفتحها." ,
  "title" :"ADE - Access Project Extension File" ,
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
} ,
  "lastmod" : "2021-08-29"
}

## ما هو ملف ADE؟

الملف بملحق .ade هو ملف Microsoft Access Project يحتوي على الإخراج المترجم للمعلومات الموجودة في ملف مشروع Microsoft Access ADP. تتوفر المعلومات الموجودة في ملف مشروع Access ، بخلاف Visual Basic for Applications (VBA) ، في نموذج مجمع في ملفات ADE. يتم تخزين البيانات بتنسيق مضغوط في هذه الملفات لتقليل حجم الملف وتحسين الأداء في Access. نظرًا لأن ADE هو الإخراج المترجم لملف مشروع Access ، فإن أي كود مصدر لـ VBA يعد جزءًا من المشروع ، يظل محميًا بعدم السماح له بأن يكون جزءًا من الإخراج. يمكن فتح ملفات ADE في Microsoft Access 365.

## تنسيق ملف ADE - مزيد من المعلومات

ADE هي ملفات قاعدة بيانات Access مجمعة يتم تخزينها على القرص كملفات ثنائية. هيكل الملف الداخلي لهذه الملفات غير معروف.

يمكن أن تخلق ملفات ADE مشكلات في الفتح استنادًا إلى إصدار Microsoft Access الذي تم استخدامه لإنشاء هذه الملفات. قواعد بيانات الوصول التي تستخدم الإصدار 64 بت من Microsoft Access 2010 والتي تم تجميعها برمجية كـ MDE أو [ACCDE] (/ar/ database / accde /) أو ملفات ADE يجب إعادة تجميعها في Microsoft Access 2021 Service Pack 1 (SP1) العمل بشكل صحيح مع Access 2010 SP1. تحدث هذه المشكلة لأن Access 2010 SP1 يستخدم إصدارًا أحدث من ملف VBE7.dll (الإصدار 7.00.1619).

## مراجع

* [مشكلة في الوصول إلى ملفات ADE] (https://docs.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [ما هي تنسيقات ملفات الوصول المراد استخدامها] (https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

