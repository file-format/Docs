{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DDS-Dateiformat – DirectDraw-Oberflächenbilddatei",
  "description":"Erfahren Sie mehr über das DDS-Dateiformat und APIs, die DDS-Dateien erstellen und öffnen können.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## Was ist eine DDS-Datei?

Eine DDS-Datei ist eine Rasterbilddatei, die das Containerformat DirectDraw Surface (DDS) verwendet. Es speichert unkomprimierte und komprimierte (DXTn) Texturen und implementiert verschiedene Typen zum Speichern verschiedener Datentypen. Es unterstützt auch verschiedene Arten von Daten wie Texturen mit einer Ebene, Texturen mit Mipmaps, Cube-Maps, Volume-Maps und Textur-Arrays. Dadurch können die DDS-Dateien zusätzlich zu digitalen Fotos und Windows-Desktop-Hintergründen Textureinheitsmodelle von Videospielen speichern. Das DDS-Dateiformat wurde von Microsoft für die Verwendung mit DirectX SDK entwickelt.

## DDS-Dateiformat

DDS-Dateien werden als Binärdateien gespeichert und können mit DirectX SDK verwendet werden. Es nutzt die Leistungsfähigkeit von DirectX, um Echtzeit-Rendering-Anwendungen wie 3D-Spiele zu entwickeln.

### Layout der DDS-Datei

Das [DDS-Dateilayout](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) wurde von Microsoft ausführlich dokumentiert. Eine binäre DDS-Datei enthält die folgenden Informationen.

* Ein DWORD (magische Zahl), das den vierstelligen Codewert „DDS“ (0x20534444) enthält.
* Eine Beschreibung der Daten in der Datei.

Der DDS_HEADER beschreibt die Daten und der DDS_PIXELFORMAT beschreibt das Pixelformat. Diese ersetzen beide die veralteten DirectDraw 7-Strukturen DDSURFACEDESC2, DDSCAPS2 und DDPIXELFORMAT.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

Der [Programmierleitfaden für das DDS-Dateiformat] (https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) führt die technischen Details dieses Dateiformats weiter aus.

## Verweise

* [DDS – von Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [Technisches Referenzhandbuch für das ZSoft PCX-Dateiformat](http://qzx.com/pc-gpe/pcx.txt)

