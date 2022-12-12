{
  "date" : "2020-08-20",
  "keywords" :[ "soubor sdf", "formát souboru sdf", "co je soubor sdf", "soubor", "příklad sdf", "přípona souboru sdf", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - Formát databáze písem Spline",
  "description":"Další informace o formátu souboru SFD a rozhraních API, která mohou vytvářet a otevírat soubory SFD.",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## Co je soubor SFD?

Soubor s příponou .sfd (Spline Font Database) je nativní formát písem ASCII pro software pro úpravu písem - FontForge. Software podporuje mnoho dalších běžných formátů písem a je volně dostupný. Software lze použít pro téměř všechny moderní operační systémy včetně Linuxu, Windows a MacOS.

## **Formát souboru SFD**
Soubory SFD jsou soubory ASCII, které jsou čitelné pro člověka a snadno se přenášejí přes internet. Jako typ MIME je identifikován pomocí application/vnd.font-fontforget-sfd.

### Záhlaví
Běžné záhlaví souboru SFD je znázorněno v následujícím příkladu.

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


## **Reference**

* [Formát souboru SFD od FontForge](https://fontforge.org/docs/techref/sfdformat.html)

