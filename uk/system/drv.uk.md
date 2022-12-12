{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "розширення", "файл", "формат", "система", "драйвер", "драйвер пристрою Windows", "програми", "комп'ютер", "програма"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - драйвер пристрою Windows",
  "description":"Дізнайтеся про формат файлу DRV та API, які можуть створювати та відкривати файли DRV.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Що таке файл DRV? ##

Файли з розширенням .drv належать до драйвера пристрою Windows. Операційна система Windows використовує ці файли для підключення внутрішніх і зовнішніх жорстких пристроїв. Файли DRV складаються з інструкцій і параметрів зв’язку між пристроєм і операційною системою. Ці файли допомагають встановити драйвери пристроїв для належної роботи з Windows. Крім того, для пристроїв, підключених до материнської плати ПК через шину або кабель, потрібні файли DRV.


## Формат файлу DRV ##

Файли DRV зазвичай упаковуються як динамічні бібліотеки (файли [DDL](/uk/system/dll/)) або файли [EXE](/uk/executable/exe/). Ці файли можуть підтримуватися на всіх системних платформах, таких як смартфони, і немає гарантії, що кожна платформа підтримуватиме ці файли належним чином. Однак деякі найпоширеніші пристрої, які використовують розширення файлу .drv:

* Звукові карти
* Графічні карти
* Принтери
* Пристрої зберігання
* Мережеві адаптери
* Комплектуючі до комп’ютерного обладнання

Рекомендується не відкривати файли DRV, надіслані електронною поштою, оскільки цей формат містить віруси та інші шкідливі програми. Обов’язково виконайте комплексне сканування, перш ніж відкривати будь-який невідомий файл DRV.


## Приклад DRV ##

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

