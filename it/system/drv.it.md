{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "estensione", "file", "formato", "sistema", "Driver", "Driver dispositivo Windows", "programmi", "computer", "applicazione" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Driver di dispositivo Windows",
  "description":"Scopri il formato di file DRV e le API che possono creare e aprire file DRV.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Che cos'è un file DRV? ##

I file con estensione .drv appartengono al driver di dispositivo di Windows. Il sistema operativo Windows utilizza questi file per collegare dispositivi rigidi interni ed esterni. I file DRV sono costituiti da istruzioni e parametri su come un dispositivo e un sistema operativo si collegano insieme. Questi file aiutano a installare i driver di dispositivo per il corretto funzionamento con Windows. Inoltre, i dispositivi collegati alla scheda madre del PC tramite bus o cavo richiedono file DRV.


## Formato file DRV ##

I file DRV sono solitamente impacchettati come librerie dinamiche (file [DDL](/it/system/dll/)) o [EXE](/it/executable/exe/). Questi file possono essere supportati su tutte le piattaforme di sistema, come gli smartphone, e non vi è alcuna garanzia che ciascuna piattaforma supporterà correttamente questi file. Tuttavia, alcuni dispositivi più comuni che utilizzano l'estensione del file .drv sono:

* Schede audio
* Schede grafiche
* Stampanti
* Dispositivi di memoria
* Adattatori di rete
* Accessori hardware per computer

Si consiglia di non aprire i file DRV inviati tramite e-mail perché questo formato di file contiene virus e altri programmi dannosi. Assicurati di eseguire una scansione completa prima di aprire qualsiasi file DRV sconosciuto.


## Esempio DRV ##

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

