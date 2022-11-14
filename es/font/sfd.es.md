{
  "date" : "2020-08-20",
  "keywords" :[ "archivo sdf", "formato de archivo sdf", "qué es un archivo sdf", "archivo", "ejemplo sdf", "extensión de archivo sdf","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - Formato de base de datos de fuentes Spline",
  "description":"Obtenga información sobre el formato de archivo SFD y las API que pueden crear y abrir archivos SFD",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## ¿Qué es un archivo SFD?

Un archivo con la extensión .sfd (base de datos de fuentes Spline) es un formato de fuente ASCII nativo para el software de edición de fuentes: FontForge. El software es compatible con muchos otros formatos de fuentes comunes y está disponible gratuitamente. El software se puede utilizar para casi todos los sistemas operativos modernos, incluidos Linux, Windows y MacOS.

## **Formato de archivo SFD**
Los archivos SFD son archivos ASCII que son legibles por humanos y se transfieren fácilmente a través de Internet. Se identifica mediante application/vnd.font-fontforget-sfd como su tipo MIME.

### Encabezado
Un encabezado de archivo SFD común se muestra en el siguiente ejemplo.

```
SplineFontDB: 3.0
FontName: Ambrosia
FullName: Ambrosia
FamilyName: Ambrosia
DefaultBaseFilename: Ambrosia-1.0
Weight: Medium
Copyright: Copyright (C) 1995-2000 by George Williams
Comments: This is a funny font.
UComments: "This is a funny font."
FontLog: "Create Jan 2008"
Version: 001.000
ItalicAngle: 0
UnderlinePosition: -133
UnderlineWidth: 20
Ascent: 800
Descent: 200
sfntRevision: 0x00078106
WidthSeparation: 140
LayerCount: 4
Layer: 0 0 "Back" 1
Layer: 1 1 "Fore" 0
Layer: 2 0 "Cubic_Fore" 0
Layer: 3 0 "Test" 1
DisplaySize: -24
DisplayLayer: 1
AntiAlias: 1
WinInfo: 64 16 4
FitToEm: 1
UseUniqueID: 0
UseXUID: 1
XUID: 3 18 21
Encoding: unicode
Order2: 1
OnlyBitmaps: 0
MacStyle: 0
TeXData: 1 10485760 0 269484 134742 89828 526385 1048576 89828
CreationTime: 1151539072
ModificationTime: 11516487392
GaspTable 3 8 2 16 1 65535 3 0
DEI: 91125
ExtremaBound: 30
```


## **Referencias**

* [Formato de archivo SFD de FontForge](https://fontforge.org/docs/techref/sfdformat.html)

