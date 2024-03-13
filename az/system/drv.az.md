{
  "date": "2021-07-08",
  "keywords": [
"DRV",
"uzadılması",
"fayl",
"format",
"sistemi",
"Sürücü",
"Windows cihaz sürücü",
"proqramlar",
"kompüter",
"tətbiq"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DRV - Windows Cihaz Sürücüsü",
  "description": "DRV fayl formatı və DRV faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "DRV",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dr-azv"
}
},
  "lastmod": "2021-07-08"
}

## DRV faylı nədir? ##

.drv uzantısı olan fayllar Windows Device Driver-a aiddir. Windows Əməliyyat Sistemi bu faylları daxili və xarici sərt cihazları birləşdirmək üçün istifadə edir. DRV faylları cihazın və əməliyyat sisteminin bir-birinə necə bağlanması ilə bağlı təlimat və parametrlərdən ibarətdir. Bu fayllar Windows ilə düzgün işləmək üçün cihaz drayverlərini quraşdırmağa kömək edir. Həmçinin, avtobus və ya kabel vasitəsilə PC-nin ana platasına qoşulan qurğular DRV faylları tələb edir.


## DRV Fayl Formatı ##

DRV faylları adətən dinamik kitabxanalar ([DDL](/system/dll/) faylları) və ya [EXE](/executable/exe/) faylları kimi paketlənir. Bu fayllar smartfonlar kimi bütün sistem platformalarında dəstəklənə bilər və hər bir platformanın bu faylları lazımi şəkildə dəstəkləyəcəyinə əminlik yoxdur. Bununla belə, .drv fayl uzantısından istifadə edən ən çox yayılmış bəzi cihazlar bunlardır:

* Səs kartları
* Qrafik kartları
* Printerlər
* Saxlama cihazları
* Şəbəkə adapterləri
* Kompüter avadanlığı aksesuarları

E-poçt vasitəsilə göndərilən DRV fayllarını açmamaq tövsiyə olunur, çünki bu fayl formatında viruslar və digər zərərli proqramlar var. Hər hansı naməlum DRV faylını açmadan əvvəl hərtərəfli skan etdiyinizə əmin olun.


## DRV Nümunəsi ##

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

