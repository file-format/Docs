{
  "date" : "2020-11-11",
  "keywords" :["ACCDB" , "امتداد" , "ملف" , "تنسيق الملف" , "نوع ملف قاعدة البيانات" , "تنسيق ملف قاعدة البيانات" , "ملفات قاعدة البيانات"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف ACCDB وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات ACCDB وفتحها." ,
  "title" :"تنسيق ملف ACCDB - ملف قاعدة بيانات Microsoft Access 2007" ,
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
} ,
  "lastmod" : "2020-11-12"
}

## ما هو ملف ACCDB؟

الملف بامتداد accdb. هو ملف قاعدة بيانات Microsoft Access 2007 يخزن بيانات المستخدمين في جداول. يدعم التخزين
النماذج المخصصة واستعلامات SQL والبيانات الأخرى. استبدلت ملفات ACCDB ملفات [MDB](/ar/database/mdb/) بعد أن تحولت Microsoft إلى بنية ملف تستند إلى XML. لا يزال من الممكن تحويل ملفات ACCDB إلى MDB بالتوافق القديم. ومع ذلك ، فإن ACCDB هو تنسيق ملف قاعدة بيانات Access المستخدم على نطاق واسع الآن. دعمت Microsoft أيضًا ميزات إضافية بتنسيق ACCDB مثل إمكانية تخزين مرفقات الملفات والبيانات الثنائية والدعم الميداني متعدد القيم.

## تنسيق ملف ACCDB

مثل MDB ، لا توجد مواصفات عامة متاحة لتنسيق ملف ACCDB. تدعم Microsoft الوصول إلى هذه الملفات برمجيًا عبر معيار Open Database Connectivity (ODBC) و Visual Basic for Applications (VBA).

### فكرة

يشير تفريغ سداسي عشرية لملف ACCDB بسيط إلى وجود أوجه تشابه عامة في البنية مع أحدث إصدارات عائلة تنسيق MDB السابقة. يستخدم كلا تنسيقي الملفات أحجام صفحات ثابتة تبلغ 4096 بايت. تشابه آخر بين ACCDB و MDB هو شكل الرقم السحري ، والذي يتضمن السلسلة "Standard ACE DB" لـ ACCDB. يوجد إصدار أو كود التوافق في نفس الموقع في كلا التنسيقين. إن mdbtools | حالات ملف القرصنة "يحتوي Offset 0x14 على إصدار Jet من قاعدة البيانات هذه" ويوافق دليل MDB غير الرسمي. تشير المعلومات الواردة في هذه المصادر ، جنبًا إلى جنب مع إدخال Wikipedia لـ [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine) ، إلى أن القيمة 0x02 تشير إلى ACE 12 (Access 2007) و 0x03 تشير إلى ACE 14 (أكسس 2010). ومع ذلك ، فإن الحد الأدنى من قاعدة البيانات التي تم إنشاؤها في Access 2010 وقاعدة مماثلة تم إنشاؤها في Access 2016 يحتوي كلاهما على 0x02 في هذا الموقع. الحد الأدنى لقاعدة البيانات التي تم إنشاؤها في Access 2016 ، ولكن تحديد عمود بنوع بيانات "عدد صحيح كبير" الذي تم تقديمه حديثًا ، له قيمة 0x05. في ملفات ACCDB ، يبدو أن هذا المؤشر يعكس توافق الملف بدلاً من إصدار محرك ACE المستخدم لإنشائه.

## مراجع

* [مواصفات Access 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [محرك قاعدة بيانات Microsoft Jet](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [ما تنسيق ملف Access الذي يجب استخدامه؟](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)
