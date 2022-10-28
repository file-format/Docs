{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "Erweiterung", "Datei", "Format", "System", "Treiber", "Windows-Gerätetreiber", "Programme", "Computer", "Anwendung" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Windows-Gerätetreiber",
  "description":"Erfahren Sie mehr über das DRV-Dateiformat und APIs, die DRV-Dateien erstellen und öffnen können.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Was ist eine DRV-Datei? ##

Die Dateien mit der Erweiterung .drv gehören zum Windows-Gerätetreiber. Das Windows-Betriebssystem verwendet diese Dateien, um interne und externe Festplatten zu verbinden. DRV-Dateien bestehen aus Anweisungen und Parametern für die Verknüpfung von Gerät und Betriebssystem. Diese Dateien helfen bei der Installation von Gerätetreibern für das ordnungsgemäße Funktionieren mit Windows. Auch die per Bus oder Kabel mit der Hauptplatine des PCs verbundenen Geräte benötigen DRV-Dateien.


## DRV-Dateiformat ##

DRV-Dateien werden normalerweise als dynamische Bibliotheken ([DDL](/de/system/dll/)-Dateien) oder [EXE](/de/executable/exe/)-Dateien gepackt. Diese Dateien können auf allen Systemplattformen wie Smartphones unterstützt werden, und es gibt keine Garantie dafür, dass jede Plattform diese Dateien ordnungsgemäß unterstützt. Einige der gängigsten Geräte, die die Dateierweiterung .drv verwenden, sind jedoch:

* Soundkarten
* Grafikkarten
* Drucker
* Speichergeräte
* Netzwerkadapter
* Computer-Hardware-Zubehör

Es wird empfohlen, per E-Mail gesendete DRV-Dateien nicht zu öffnen, da dieses Dateiformat Viren und andere Schadprogramme enthält. Stellen Sie sicher, dass Sie einen umfassenden Scan durchführen, bevor Sie eine unbekannte DRV-Datei öffnen.


## DRV-Beispiel ##

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

