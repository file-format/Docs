{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "kiterjesztés", "fájl", "formátum", "rendszer", "illesztőprogram", "Windows Device Driver", "programok", "számítógép", "alkalmazás" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Windows eszközillesztő",
  "description":"További információ a DRV fájlformátumról és az API-król, amelyek DRV fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Mi az a DRV fájl? ##

A .drv kiterjesztésű fájlok a Windows eszközillesztőhöz tartoznak. A Windows operációs rendszer ezeket a fájlokat használja a belső és külső mereveszközök csatlakoztatására. A DRV-fájlok utasításokat és paramétereket tartalmaznak, amelyek segítségével az eszköz és az operációs rendszer hogyan kapcsolódik egymáshoz. Ezek a fájlok segítenek az eszközillesztők telepítésében a Windows rendszerrel való megfelelő működés érdekében. Ezenkívül a számítógép alaplapjához buszon vagy kábelen keresztül csatlakoztatott eszközök DRV-fájlokat igényelnek.


## DRV fájlformátum ##

A DRV-fájlok általában dinamikus könyvtárakba ([DDL](/hu/system/dll/)) vagy [EXE](/hu/executable/exe/) fájlokba vannak csomagolva. Ezek a fájlok minden rendszerplatformon, például okostelefonokon támogathatók, és nincs garancia arra, hogy mindegyik platform megfelelően támogatja ezeket a fájlokat. A .drv fájlkiterjesztést használó leggyakoribb eszközök azonban a következők:

* Hangkártyák
* Grafikus kártyák
* Nyomtatók
* Tárolóeszközök
* Hálózati adapterek
* Számítógépes hardver tartozékok

Javasoljuk, hogy ne nyissa meg az e-mailben küldött DRV fájlokat, mert ez a fájlformátum vírusokat és más rosszindulatú programokat tartalmaz. Minden ismeretlen DRV fájl megnyitása előtt végezzen átfogó vizsgálatot.


## DRV példa ##

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

