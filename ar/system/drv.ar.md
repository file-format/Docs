{
  "date" : "2021-07-08",
  "keywords" :["DRV", "extension", "file", "format", "system", "Driver", "Windows Device Driver", "Programs", "computer", "application"],
  "author" : {
    "display_name" : "Sami Cheema"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - برنامج تشغيل جهاز Windows" ,
  "description":"تعرف على تنسيق ملف DRV وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات DRV وفتحها." ,
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
} ,
  "lastmod" : "2021-07-08"
}

## ما هو ملف DRV؟ ##

تنتمي الملفات ذات الامتداد .drv إلى برنامج تشغيل جهاز Windows. يستخدم نظام التشغيل Windows هذه الملفات لتوصيل الأجهزة الصلبة الداخلية والخارجية. تتكون ملفات DRV من تعليمات ومعلمات لكيفية ارتباط الجهاز ونظام التشغيل معًا. تساعد هذه الملفات في تثبيت برامج تشغيل الجهاز من أجل حسن سير العمل مع Windows. أيضًا ، تتطلب الأجهزة المرتبطة باللوحة الأم للكمبيوتر الشخصي عبر ناقل أو كبل ملفات DRV.


## تنسيق ملف DRV ##

عادةً ما يتم حزم ملفات DRV كمكتبات ديناميكية (ملفات [DDL] (/ar/ system / dll /)) أو ملفات [EXE] (/ar/ قابل للتنفيذ / exe /). يمكن دعم هذه الملفات على جميع الأنظمة الأساسية ، مثل الهواتف الذكية ، وليس هناك ما يضمن أن كل منصة ستدعم هذه الملفات بشكل صحيح. ومع ذلك ، فإن بعض الأجهزة الأكثر شيوعًا التي تستخدم امتداد الملف .drv هي:

* كروت صوت
* كروت جرافيك
* طابعات
* أجهزة التخزين
* محولات الشبكة
* ملحقات أجهزة الكمبيوتر

يوصى بعدم فتح ملفات DRV المرسلة عبر البريد الإلكتروني لأن تنسيق الملف هذا يحتوي على فيروسات وبرامج ضارة أخرى. تأكد من إجراء فحص شامل قبل فتح أي ملف DRV غير معروف.


## مثال DRV ##

```
// Include necessary files...
#include <font.defs>
#include <media.defs>
#include <hp.h>
#include <epson.h>
#include <label.h>

// Localizations are provided for all of the base languages supported by
// CUPS...
#po ar ""
#po ca ""
#po de ""
#po el ""
#po es ""
#po fr ""
#po no ""
#po ru ""
#po sk ""
#po sv ""
#po th ""
#po tr ""
#po uk ""

// MediaSize sizes used by label drivers...
#media "w90h18/1.25x0.25\"" 90 18
#media "w90h162/1.25x2.25\"" 90 162
#media "w108h18/1.50x0.25\"" 108 18
#media "w108h36/1.50x0.50\"" 108 36
#media "w108h72/1.50x1.00\"" 108 72
#media "w108h144/1.50x2.00\"" 108 144
#media "w144h26/2.00x0.37\"" 144 26
#media "w576h360/8.00x5.00\"" 576 360
#media "w576h432/8.00x6.00\"" 576 432
#media "w576h468/8.00x6.50\"" 576 468

// Common stuff for all drivers...
Attribute "cupsVersion" "" "2.2"
Attribute "FileSystem" "" "False"
Attribute "LandscapeOrientation" "" "Plus90"
Attribute "TTRasterizer" "" "Type42"

Font *

Version "2.1"

// Dymo Label Printer
{
  Manufacturer "Dymo"
  ModelName "Label Printer"
  Attribute NickName "" "Dymo Label Printer"
  PCFileName "dymo.ppd"
  DriverType label
  ModelNumber $DYMO_3x0
  Throughput 8
  ManualCopies Yes
  ColorDevice No

  HWMargins 2 14.9 2 14.9

  *MediaSize w81h252
  MediaSize w101h252
  MediaSize w54h144
  MediaSize w167h288
  MediaSize w162h540
  MediaSize w162h504
  MediaSize w41h248
  MediaSize w41h144
  MediaSize w153h198

  Resolution k 1 0 0 0 136dpi
  Resolution k 1 0 0 0 203dpi
  *Resolution k 1 0 0 0 300dpi

  Darkness 0 Light
  Darkness 1 Medium
  *Darkness 2 Normal
  Darkness 3 Dark
}

```

