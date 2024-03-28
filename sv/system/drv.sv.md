{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "tillägg", "fil", "format", "system", "Drivrutin", "Windows-enhetsdrivrutin", "program", "dator", "applikation" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Windows Device Driver",
  "description":"Läs mer om DRV-filformat och API:er som kan skapa och öppna DRV-filer.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Vad är DRV fil? ##

Filerna med filtillägget .drv tillhör Windows enhetsdrivrutin. Windows operativsystem använder dessa filer för att ansluta interna och externa hårda enheter. DRV-filer består av instruktioner och parametrar för hur en enhet och ett operativsystem länkar ihop. Dessa filer hjälper till att installera drivrutiner för korrekt funktion med Windows. De enheter som är kopplade till datorns moderkort via buss eller kabel kräver också DRV-filer.


## DRV-filformat ##

DRV-filer är vanligtvis paketerade som dynamiska bibliotek ([DDL](/sv/system/dll/)-filer) eller [EXE](/sv/executable/exe/)-filer. Dessa filer kan stödjas på alla systemplattformar, till exempel smartphones, och det finns ingen garanti för att varje plattform kommer att stödja dessa filer korrekt. Några vanligaste enheter som använder filtillägget .drv är dock:

* Ljudkort
* Grafikkort
* Skrivare
* Lagringsenheter
* Nätverksadaptrar
* Tillbehör till datorhårdvara

Det rekommenderas att inte öppna DRV-filer som skickas via e-post eftersom detta filformat innehåller virus och andra skadliga program. Se till att utföra en omfattande genomsökning innan du öppnar någon okänd DRV-fil.


## DRV Exempel ##

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

