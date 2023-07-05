{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف TCX- ملف XML لمركز التدريب" ,
  "description":"تعرف على تنسيق ملف TCX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات TCX وفتحها." ,
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
} ,
  "lastmod" : "2022-05-06"
}

## ما هو ملف TCX؟

ملف TCX (مركز التدريب XML) هو تنسيق لتبادل البيانات يستخدم لمشاركة البيانات بين أجهزة اللياقة البدنية. تم تقديمه في عام 2008 مع منتج مركز تدريب Garmin. يتم تخزين بيانات التمرين مثل معدل ضربات القلب وإيقاع الجري وإيقاع الدراجات والسعرات الحرارية ووقت الدورة بتنسيق [XML](/ar/web/xml/) داخل ملف TCX. بالإضافة إلى ذلك ، يتم أيضًا تضمين بيانات موجزة حول مسار التمرين في ملف TCX. تشبه ملفات TCX ملفات [FIT](/ar/gis/fit/) التي تم إنشاؤها باستخدام أجهزة Garmin الرياضية القابلة للارتداء.

## تنسيق ملف TCX - مزيد من المعلومات

يتم حفظ ملفات TCX على القرص كملفات XML مع حفظ كل سجل كنشاط. يشتمل النشاط على جميع بيانات التمرين مثل الوقت ووقت الدورة والمعرف ومعدل ضربات القلب والشدة والإيقاع ومعلومات المسار التي تحتوي على أزواج من الموضع جنبًا إلى جنب مع الطابع الزمني لموضع خط الطول هذا المماثل لـ [GPX](/ar/gis/gpx/) الملفات.

### إصدارات تنسيق ملف TCX

يوجد إصداران من هذا التنسيق مع مخططات XML الخاصة بهما والتي تستضيفها Garmin. فيما يلي عدد قليل منهم:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## بروتوكول بيانات TCX

يتوفر إصدار سريع من تنسيق TCX XML على Github كـ [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## مراجع ##

* [مركز التدريب XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

