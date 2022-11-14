{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "extensie", "bestand", "format", "systeem", "stuurprogramma", "Windows-apparaatstuurprogramma", "programma's", "computer", "toepassing"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Windows-apparaatstuurprogramma",
  "description":"Meer informatie over DRV-bestandsindeling en API's die DRV-bestanden kunnen maken en openen.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Wat is een DRV-bestand? ##

De bestanden met de extensie .drv behoren tot de Windows Device Driver. Windows-besturingssysteem gebruikt deze bestanden om interne en externe harde apparaten aan te sluiten. DRV-bestanden bestaan uit instructies en parameters voor hoe een apparaat en besturingssysteem met elkaar verbonden zijn. Deze bestanden helpen bij het installeren van apparaatstuurprogramma's voor een goede werking met Windows. Ook hebben de apparaten die via bus of kabel met het moederbord van de pc zijn verbonden, DRV-bestanden nodig.


## DRV-bestandsindeling ##

DRV-bestanden zijn meestal verpakt als dynamische bibliotheken ([DDL](/nl/system/dll/)-bestanden) of [EXE](/nl/executable/exe/)-bestanden. Deze bestanden kunnen worden ondersteund op alle systeemplatforms, zoals smartphones, en er is geen garantie dat elk platform deze bestanden naar behoren zal ondersteunen. Sommige meest voorkomende apparaten die de .drv-bestandsextensie gebruiken, zijn echter:

* Geluidskaarten
* Grafische kaarten
* Printers
* Opslagapparaten
* Netwerkadapters
* Accessoires voor computerhardware

Het wordt aanbevolen om geen DRV-bestanden te openen die via e-mail zijn verzonden, omdat dit bestandsformaat virussen en andere schadelijke programma's bevat. Zorg ervoor dat u een uitgebreide scan uitvoert voordat u een onbekend DRV-bestand opent.


## DRV-voorbeeld ##

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

