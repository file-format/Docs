{
  "date" : "2021-07-08",
  "keywords" :["DRV", "rozszerzenie", "plik", "format", "system", "Sterownik", "Sterownik urządzenia Windows", "programy", "komputer", "aplikacja"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV – sterownik urządzenia Windows",
  "description":"Poznaj format pliku DRV i interfejsy API, które mogą tworzyć i otwierać pliki DRV.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Czym jest plik DRW? ##

Pliki z rozszerzeniem .drv należą do sterownika urządzenia systemu Windows. System operacyjny Windows używa tych plików do łączenia wewnętrznych i zewnętrznych urządzeń twardych. Pliki DRV składają się z instrukcji i parametrów dotyczących sposobu łączenia urządzenia i systemu operacyjnego. Pliki te pomagają zainstalować sterowniki urządzeń do prawidłowego funkcjonowania z systemem Windows. Ponadto urządzenia połączone z płytą główną komputera za pośrednictwem magistrali lub kabla wymagają plików DRV.


## Format pliku DRV ##

Pliki DRV są zwykle pakowane jako biblioteki dynamiczne (pliki [DDL](/pl/system/dll/)) lub [EXE](/pl/executable/exe/). Pliki te mogą być obsługiwane na wszystkich platformach systemowych, takich jak smartfony i nie ma gwarancji, że każda platforma będzie poprawnie obsługiwać te pliki. Jednak niektóre najczęstsze urządzenia korzystające z rozszerzenia pliku .drv to:

* Karty dźwiękowe
* Karty graficzne
* Drukarki
* Urządzenia pamięci masowej
* Karty sieciowe
* Akcesoria do sprzętu komputerowego

Zaleca się, aby nie otwierać plików DRV wysyłanych pocztą elektroniczną, ponieważ ten format plików zawiera wirusy i inne złośliwe programy. Upewnij się, że wykonałeś kompleksowe skanowanie przed otwarciem jakiegokolwiek nieznanego pliku DRV.


## Przykład DRV ##

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

