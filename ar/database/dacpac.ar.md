{
  "date" : "2021-09-06",
  "keywords" :["dacpac" , "extension" , "file" , "تنسيق الملف" , "نوع ملف قاعدة البيانات" , "تنسيق ملف قاعدة البيانات" , "حزمة تطبيق طبقة البيانات"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف DACPAC وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات DACPAC وفتحها." ,
  "title" :"DACPAC - حزمة تطبيق مستوى البيانات" ,
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
} ,
  "lastmod" : "2021-09-06"
}

## ما هو ملف DACPAC؟

الملف بامتداد .dacpac (يرمز إلى Data Tier AppliCation Package) هو ملف قاعدة بيانات ، تم إنشاؤه باستخدام تطبيق طبقة بيانات Microsoft SQL Server ، والذي يحتوي على نموذج قاعدة البيانات لتمثيل كائنات قاعدة البيانات. نظرًا لاحتوائه على النموذج الكامل لقاعدة البيانات ، يتم استخدامه لاستعادة قاعدة البيانات من التفاصيل المتاحة في النموذج. عادةً ما يتم تسليم ملفات DACPAC إلى فرق النشر لتثبيتها في مقر العميل لاستعادة قاعدة البيانات. يمكن فتح هذه باستخدام
Microsoft SQL Server 2019 =1&OCID=AID2200057_aff_7593_1243925&tduid=%28ir__gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00%29%287593%29%281243925%29%284LioSo.jxMc-XSp30B6cXpiTS89wo0jYzw%29%28%29&irclickid=_gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00).

## تنسيق ملف DACPAC - مزيد من المعلومات

ملفات حزمة بيانات DACPAC هي في الواقع ملفات مضغوطة من نوع ZIP تحتوي على عدة ملفات [XML](/ar/ web / xml /) تحتوي على معلومات حول نموذج قاعدة البيانات ، مثل الجداول وطرق العرض ، المستخدمة لاستعادة قاعدة البيانات. لعرض محتويات ملفات DACPAC ، أعد تسمية الملفات من .dacpac إلى [.zip](/ar/ compression / zip /) واستخرج الأرشيف المضغوط باستخدام أي أداة مساعدة لفك الضغط.

فيما يلي بعض الملفات التي تم العثور عليها داخل ملف DACPAC.

* [أنواع المحتوى] .xml
""
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns = "http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
""
* DacMetadata.xml

""
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
""
* الأصل. xml

* model.xml

وتجدر الإشارة إلى أن DACPAC لا يحتوي على بيانات وكائنات أخرى على مستوى الخادم. يمكن أن يحتوي الملف على جميع أنواع الكائنات التي قد يتم الاحتفاظ بها في مشروع SSDT.

## مراجع

* [تطبيقات طبقة البيانات - الفوائد](https://docs.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications؟view=sql-server-ver15)
* [نشر تطبيق طبقة البيانات - Microsoft](https://docs.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [كيف تنشئ ملف DACPAC؟](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

