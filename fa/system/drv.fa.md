{
  "date": "2021-07-08",
  "keywords": [
"DRV",
"افزونه",
"فایل",
"قالب",
"سیستم",
"راننده",
"درایور دستگاه ویندوز",
"برنامه ها",
"کامپیوتر",
"کاربرد"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DRV - درایور دستگاه ویندوز",
  "description": "درباره فرمت فایل DRV و APIهایی که می‌توانند فایل‌های DRV را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "DRV",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dr-fav"
}
},
  "lastmod": "2021-07-08"
}

## فایل DRV چیست؟ ##

فایل های با پسوند .drv متعلق به درایور دستگاه ویندوز هستند. سیستم عامل ویندوز از این فایل ها برای اتصال دستگاه های سخت داخلی و خارجی استفاده می کند. فایل‌های DRV شامل دستورالعمل‌ها و پارامترهایی برای نحوه پیوند دستگاه و سیستم‌عامل با هم هستند. این فایل ها به نصب درایورهای دستگاه برای عملکرد مناسب با ویندوز کمک می کنند. همچنین، دستگاه‌های متصل به مادربرد رایانه شخصی از طریق گذرگاه یا کابل به فایل‌های DRV نیاز دارند.


## فرمت فایل DRV ##

فایل‌های DRV معمولاً به‌عنوان کتابخانه‌های پویا (فایل‌های [DDL](/system/dll/)) یا [EXE](/executable/exe/) بسته‌بندی می‌شوند. این فایل ها را می توان در تمامی پلتفرم های سیستم مانند گوشی های هوشمند پشتیبانی کرد و هیچ اطمینانی وجود ندارد که هر پلتفرم به درستی از این فایل ها پشتیبانی کند. با این حال، برخی از رایج ترین دستگاه هایی که از پسوند فایل .drv استفاده می کنند عبارتند از:

* کارت های صدا
* کارت های گرافیک
* چاپگرها
* دستگاه های ذخیره سازی
* آداپتورهای شبکه
* لوازم جانبی سخت افزار کامپیوتر

توصیه می شود فایل های DRV ارسال شده از طریق ایمیل را باز نکنید زیرا این فرمت فایل حاوی ویروس ها و سایر برنامه های مخرب است. قبل از باز کردن هر فایل DRV ناشناخته، مطمئن شوید که یک اسکن جامع انجام داده اید.


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

