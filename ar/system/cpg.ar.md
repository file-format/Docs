{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف CPG - ملف صفحة رمز ESRI" ,
  "description":"تعرف على تنسيق ملف CPG وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CPG وفتحها." ,
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
} ,
  "lastmod" : "2022-09-01"
}

## ما هو ملف CPG؟

ملف CPG هو ملف اختياري مطلوب ملف أشكال ESRI المستخدم لتحديد صفحة الشفرة لتحديد مجموعة الأحرف التي سيتم استخدامها. يتم تخزينها في تنسيق ملف نص عادي وتحتوي على معلومات حول الترميز المطبق لإنشاء ملف الشكل. في حالة عدم توفر ملف CPG ، يستخدم ملف الشكل الترميز الافتراضي للنظام. يجب أن يكون لملف CPG ، إذا كان موجودًا ، نفس بادئة الملف [SHP] (/ar/ gis / shp /) ، على سبيل المثال ، roads.shp ، roads.cpg.

يمكن فتح ملفات CPG باستخدام ESRI ArcGIS Pro.

### تنسيق ملف CPG - مزيد من المعلومات

عند عرض ملف الشكل في ArcCatalog أو أي تطبيق ArcGIS آخر ، سترى فقط ملف الشكل. ولكن في الواقع ، يستخدم shapefile الملفات الأخرى المرتبطة التي تتم قراءتها بجانب ملف الشكل الرئيسي. يعد ملف CPG أيضًا أحد هذه الملفات إذا كان موجودًا جنبًا إلى جنب مع ملف SHP الرئيسي.

## مراجع

* [Shapefile file extension
] (https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

