{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "extensie", "fișier", "format", "sistem", "Driver", "Driver de dispozitiv Windows", "programe", "calculator", "aplicație"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV – Driver de dispozitiv Windows",
  "description":"Aflați despre formatul de fișier DRV și despre API-urile care pot crea și deschide fișiere DRV.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Ce este un fișier DRV? ##

Fișierele cu extensia .drv aparțin driverului de dispozitiv Windows. Sistemul de operare Windows utilizează aceste fișiere pentru a conecta dispozitive hard interne și externe. Fișierele DRV sunt compuse din instrucțiuni și parametri pentru modul în care un dispozitiv și un sistem de operare se conectează. Aceste fișiere ajută la instalarea driverelor de dispozitiv pentru o funcționare corectă cu Windows. De asemenea, dispozitivele conectate la placa de bază a PC-ului prin magistrală sau cablu necesită fișiere DRV.


## Format fișier DRV ##

Fișierele DRV sunt de obicei ambalate ca biblioteci dinamice (fișiere [DDL](/ro/system/dll/)) sau fișiere [EXE](/ro/executable/exe/). Aceste fișiere pot fi acceptate pe toate platformele de sistem, cum ar fi smartphone-urile, și nu există nicio asigurare că fiecare platformă va accepta corect aceste fișiere. Cu toate acestea, unele dispozitive cele mai comune care folosesc extensia de fișier .drv sunt:

* Plăci de sunet
* Cartele grafice
* Imprimante
* Dispozitive de stocare
* Adaptoare de rețea
* Accesorii hardware pentru computer

Se recomandă să nu deschideți fișierele DRV trimise prin e-mail, deoarece acest format de fișier conține viruși și alte programe rău intenționate. Asigurați-vă că efectuați o scanare completă înainte de a deschide orice fișier DRV necunoscut.


## Exemplu DRV ##

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

