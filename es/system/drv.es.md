{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "extensión", "archivo", "formato", "sistema", "Controlador", "Controlador de dispositivo de Windows", "programas", "computadora", "aplicación" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Controlador de dispositivo de Windows",
  "description":"Obtenga información sobre el formato de archivo DRV y las API que pueden crear y abrir archivos DRV",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## ¿Qué es un archivo DRV? ##

Los archivos con extensión .drv pertenecen al controlador de dispositivo de Windows. El sistema operativo Windows utiliza estos archivos para conectar dispositivos duros internos y externos. Los archivos DRV consisten en instrucciones y parámetros sobre cómo se vinculan un dispositivo y un sistema operativo. Estos archivos ayudan a instalar controladores de dispositivos para que funcionen correctamente con Windows. Además, los dispositivos vinculados con la placa base de la PC a través de bus o cable requieren archivos DRV.


## Formato de archivo DRV ##

Los archivos DRV generalmente se empaquetan como bibliotecas dinámicas (archivos [DDL](/es/ system / dll /)) o archivos [EXE](/es/ ejecutable / exe /). Estos archivos pueden admitirse en todas las plataformas del sistema, como los teléfonos inteligentes, y no hay garantía de que cada plataforma admita correctamente estos archivos. Sin embargo, algunos de los dispositivos más comunes que usan la extensión de archivo .drv son:

* Tarjetas de sonido
* Tarjetas gráficas
* Impresoras
* Dispositivos de almacenamiento
* Adaptadores de red
* Accesorios de hardware de computadora

Se recomienda no abrir archivos DRV enviados por correo electrónico porque este formato de archivo contiene virus y otros programas maliciosos. Asegúrese de realizar un análisis completo antes de abrir cualquier archivo DRV desconocido.


## DRV Ejemplo ##

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

