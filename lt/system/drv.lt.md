{
  "date": "2021-07-08",
  "keywords": [
"DRV",
"pratęsimas",
"failą",
"formatu",
"sistema",
"Vairuotojas",
"Windows įrenginio tvarkyklė",
"programas",
"kompiuteris",
"taikymas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DRV – „Windows“ įrenginio tvarkyklė",
  "description": "Sužinokite apie DRV failo formatą ir API, kurios gali kurti ir atidaryti DRV failus.",
  "linktitle": "DRV",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dr-ltv"
}
},
  "lastmod": "2021-07-08"
}

## Kas yra DRV failas? ##

Failai su plėtiniu .drv priklauso Windows įrenginio tvarkyklei. Windows operacinė sistema naudoja šiuos failus vidinių ir išorinių standžiųjų įrenginių prijungimui. DRV failus sudaro instrukcijos ir parametrai, kaip susieti įrenginys ir operacinė sistema. Šie failai padeda įdiegti įrenginių tvarkykles, kad jos tinkamai veiktų sistemoje Windows. Be to, įrenginiams, susietiems su kompiuterio pagrindine plokšte per magistralę arba kabelį, reikia DRV failų.


## DRV failo formatas ##

DRV failai paprastai supakuoti kaip dinaminės bibliotekos ([DDL](/system/dll/) failai) arba [EXE](/executable/exe/) failai. Šiuos failus galima palaikyti visose sistemos platformose, pvz., išmaniuosiuose telefonuose, ir nėra garantijos, kad kiekviena platforma tinkamai palaikys šiuos failus. Tačiau kai kurie dažniausiai naudojami įrenginiai, kuriuose naudojamas .drv failo plėtinys:

* Garso plokštės
* Grafinės kortelės
* Spausdintuvai
* Saugojimo įrenginiai
* Tinklo adapteriai
* Kompiuterinės įrangos priedai

Rekomenduojama neatidaryti DRV failų, siunčiamų el. paštu, nes šiame failo formate yra virusų ir kitų kenkėjiškų programų. Prieš atidarydami nežinomą DRV failą, būtinai atlikite išsamų nuskaitymą.


## DRV pavyzdys Nr.

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

