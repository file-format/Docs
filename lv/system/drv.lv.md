{
  "date": "2021-07-08",
  "keywords": [
"DRV",
"pagarinājumu",
"failu",
"formātā",
"sistēma",
"Šoferis",
"Windows ierīces draiveris",
"programmas",
"dators",
"pieteikumu"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DRV — Windows ierīces draiveris",
  "description": "Uzziniet par DRV faila formātu un API, kas var izveidot un atvērt DRV failus.",
  "linktitle": "DRV",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dr-lvv"
}
},
  "lastmod": "2021-07-08"
}

## Kas ir DRV fails? ##

Faili ar paplašinājumu .drv pieder Windows ierīces draiverim. Windows operētājsistēma izmanto šos failus, lai savienotu iekšējās un ārējās cietās ierīces. DRV faili sastāv no instrukcijām un parametriem ierīces un operētājsistēmas savienojumam. Šie faili palīdz instalēt ierīces draiverus, lai tie pareizi darbotos sistēmā Windows. Arī ierīcēm, kas savienotas ar datora mātesplati, izmantojot kopni vai kabeli, ir nepieciešami DRV faili.


## DRV faila formāts ##

DRV faili parasti tiek iesaiņoti kā dinamiskās bibliotēkas ([DDL](/system/dll/) faili) vai [EXE](/executable/exe/) faili. Šos failus var atbalstīt visās sistēmas platformās, piemēram, viedtālruņos, un nav garantijas, ka katra platforma pareizi atbalstīs šos failus. Tomēr dažas visizplatītākās ierīces, kurās tiek izmantots .drv faila paplašinājums, ir šādas:

* Skaņas kartes
* Grafiskās kartes
* Printeri
* Uzglabāšanas ierīces
* Tīkla adapteri
* Datortehnikas piederumi

Nav ieteicams atvērt DRV failus, kas nosūtīti pa e-pastu, jo šajā faila formātā ir vīrusi un citas ļaunprātīgas programmas. Pirms nezināma DRV faila atvēršanas noteikti veiciet visaptverošu skenēšanu.


## DRV piemērs ##

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

