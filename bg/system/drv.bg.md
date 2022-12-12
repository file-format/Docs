{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "разширение", "файл", "формат", "система", "драйвер", "драйвер на устройство на Windows", "програми", "компютър", "приложение" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Windows драйвер на устройство",
  "description":"Научете за DRV файловия формат и API, които могат да създават и отварят DRV файлове.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Какво е DRV файл? ##

Файловете с разширение .drv принадлежат на Windows Device Driver. Операционната система Windows използва тези файлове за свързване на вътрешни и външни твърди устройства. DRV файловете се състоят от инструкции и параметри за това как устройството и операционната система се свързват заедно. Тези файлове помагат за инсталиране на драйвери на устройства за правилно функциониране с Windows. Освен това устройствата, свързани с дънната платка на компютъра чрез шина или кабел, изискват DRV файлове.


## DRV файлов формат ##

DRV файловете обикновено се пакетират като динамични библиотеки ([DDL](/bg/system/dll/) файлове) или [EXE](/bg/executable/exe/) файлове. Тези файлове могат да се поддържат на всички системни платформи, като например смартфони, и няма гаранция, че всяка платформа ще поддържа правилно тези файлове. Въпреки това, някои най-често срещани устройства, които използват файловото разширение .drv, са:

* Звукови карти
* Графични карти
* Принтери
* Устройства за съхранение
* Мрежови адаптери
* Аксесоари за компютърен хардуер

Препоръчително е да не отваряте DRV файлове, изпратени по имейл, защото този файлов формат съдържа вируси и други злонамерени програми. Не забравяйте да извършите цялостно сканиране, преди да отворите неизвестен DRV файл.


## Пример за DRV ##

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

