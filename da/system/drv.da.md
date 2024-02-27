{
  "date": "2021-07-08",
  "keywords": [
"DRV",
"udvidelse",
"fil",
"format",
"system",
"Chauffør",
"Windows enhedsdriver",
"programmer",
"computer",
"Ansøgning"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DRV - Windows-enhedsdriver",
  "description": "Lær om DRV-filformat og API'er, der kan oprette og åbne DRV-filer.",
  "linktitle": "DRV",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dr-dav"
}
},
  "lastmod": "2021-07-08"
}

## Hvad er en DRV fil? ##

Filerne med filtypenavnet .drv tilhører Windows-enhedsdriveren. Windows-operativsystemet bruger disse filer til at forbinde interne og eksterne hårde enheder. DRV-filer består af instruktioner og parametre for, hvordan en enhed og et operativsystem hænger sammen. Disse filer hjælper med at installere enhedsdrivere for korrekt funktion med Windows. De enheder, der er forbundet med pc'ens bundkort via bus eller kabel, kræver også DRV-filer.


## DRV-filformat ##

DRV-filer er normalt pakket som dynamiske biblioteker ([DDL](/system/dll/) filer) eller [EXE](/executable/exe/) filer. Disse filer kan understøttes på alle systemplatforme, såsom smartphones, og der er ingen garanti for, at hver platform korrekt understøtter disse filer. Nogle mest almindelige enheder, der bruger filtypen .drv, er dog:

* Lydkort
* Grafikkort
* Printere
* Lagringsenheder
* Netværksadaptere
* Computer hardware tilbehør

Det anbefales ikke at åbne DRV-filer sendt via e-mail, fordi dette filformat indeholder vira og andre ondsindede programmer. Sørg for at udføre en omfattende scanning, før du åbner en ukendt DRV-fil.


## DRV eksempel ##

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

