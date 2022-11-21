{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "ekstensi", "file", "format", "sistem", "Driver", "Driver Perangkat Windows", "program", "komputer", "aplikasi" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Pengandar Perangkat Windows",
  "description":"Pelajari tentang format file DRV dan API yang dapat membuat dan membuka file DRV.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Apa itu file DRV? ##

File dengan ekstensi .drv milik Windows Device Driver. Sistem Operasi Windows menggunakan file-file ini untuk menghubungkan perangkat keras internal dan eksternal. File DRV terdiri dari instruksi dan parameter untuk bagaimana perangkat dan sistem operasi terhubung bersama. File-file ini membantu menginstal driver perangkat agar berfungsi dengan baik dengan Windows. Selain itu, perangkat yang terhubung dengan motherboard PC melalui bus atau kabel memerlukan file DRV.


## Format File DRV ##

File DRV biasanya dikemas sebagai pustaka dinamis (file [DDL](/id/system/dll/) atau file [EXE](/id/executable/exe/). File-file ini dapat didukung di semua platform sistem, seperti smartphone, dan tidak ada jaminan bahwa setiap platform akan mendukung file-file ini dengan baik. Namun, beberapa perangkat paling umum yang menggunakan ekstensi file .drv adalah:

* Kartu suara
* Kartu grafis
* Printer
* Perangkat penyimpanan
* Adaptor jaringan
* Aksesori perangkat keras komputer

Disarankan untuk tidak membuka file DRV yang dikirimkan melalui email karena format file ini mengandung virus dan program berbahaya lainnya. Pastikan untuk melakukan pemindaian menyeluruh sebelum membuka file DRV yang tidak dikenal.


## Contoh DRV ##

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

