{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "extension", "fichier", "format", "système", "Pilote", "Pilote de périphérique Windows", "programmes", "ordinateur", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Pilote de périphérique Windows",
  "description":"En savoir plus sur le format de fichier DRV et les API qui peuvent créer et ouvrir des fichiers DRV.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Qu'est-ce qu'un fichier DRV ? ##

Les fichiers avec une extension .drv appartiennent au pilote de périphérique Windows. Le système d'exploitation Windows utilise ces fichiers pour connecter des périphériques durs internes et externes. Les fichiers DRV sont constitués d'instructions et de paramètres sur la manière dont un périphérique et un système d'exploitation sont liés. Ces fichiers aident à installer les pilotes de périphérique pour un bon fonctionnement avec Windows. De plus, les appareils reliés à la carte mère du PC via un bus ou un câble nécessitent des fichiers DRV.


## Format de fichier DRV ##

Les fichiers DRV sont généralement conditionnés sous forme de bibliothèques dynamiques (fichiers [DDL](/fr/system/dll/)) ou [EXE](/fr/executable/exe/). Ces fichiers peuvent être pris en charge sur toutes les plates-formes système, telles que les smartphones, et rien ne garantit que chaque plate-forme prendra correctement en charge ces fichiers. Cependant, certains appareils les plus courants qui utilisent l'extension de fichier .drv sont :

* Cartes son
* Cartes graphiques
* Imprimantes
* Périphériques de stockage
* Adaptateurs réseau
* Accessoires de matériel informatique

Il est recommandé de ne pas ouvrir les fichiers DRV envoyés par e-mail car ce format de fichier contient des virus et autres programmes malveillants. Assurez-vous d'effectuer une analyse complète avant d'ouvrir un fichier DRV inconnu.


## Exemple de VRD ##

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

