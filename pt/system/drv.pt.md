{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "extensão", "arquivo", "formato", "sistema", "Driver", "Driver de dispositivo Windows", "programas", "computador", "aplicativo" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Driver de dispositivo do Windows",
  "description":"Saiba mais sobre o formato de arquivo DRV e APIs que podem criar e abrir arquivos DRV.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## O que é um arquivo DRV? ##

Os arquivos com extensão .drv pertencem ao Windows Device Driver. O sistema operacional Windows usa esses arquivos para conectar dispositivos rígidos internos e externos. Os arquivos DRV consistem em instruções e parâmetros de como um dispositivo e um sistema operacional se conectam. Esses arquivos ajudam a instalar drivers de dispositivo para um funcionamento adequado com o Windows. Além disso, os dispositivos ligados à placa-mãe do PC via barramento ou cabo requerem arquivos DRV.


## Formato de arquivo DRV ##

Os arquivos DRV geralmente são empacotados como bibliotecas dinâmicas (arquivos [DDL](/pt/system/dll/)) ou arquivos [EXE](/pt/executable/exe/). Esses arquivos podem ser suportados em todas as plataformas do sistema, como smartphones, e não há garantia de que cada plataforma oferecerá suporte adequado a esses arquivos. No entanto, alguns dispositivos mais comuns que usam a extensão de arquivo .drv são:

* Placas de som
* Placas gráficas
* Impressoras
* Dispositivos de armazenamento
* Adaptadores de rede
* Acessórios de hardware de computador

Recomenda-se não abrir arquivos DRV enviados por e-mail porque esse formato de arquivo contém vírus e outros programas maliciosos. Certifique-se de realizar uma verificação abrangente antes de abrir qualquer arquivo DRV desconhecido.


## Exemplo de DRV ##

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

