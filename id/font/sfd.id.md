{
  "date" : "2020-08-20",
  "keywords" :[ "file sdf", "format file sdf", "apa itu file sdf", "file", "contoh sdf", "ekstensi file sdf", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - Format Basis Data Font Spline",
  "description":"Pelajari tentang format file SFD dan API yang dapat membuat dan membuka file SFD.",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## Apa itu file SFD?

File dengan ekstensi .sfd (Spline Font Database) adalah format font ASCII asli untuk perangkat lunak pengedit font - FontForge. Dukungan perangkat lunak mendukung banyak format font umum lainnya dan tersedia secara bebas. Perangkat lunak ini dapat digunakan untuk hampir semua sistem operasi modern termasuk Linux, Windows, dan MacOS.

## **Format File SFD**
File SFD adalah file ASCII yang dapat dibaca manusia dan mudah ditransfer melalui internet. Itu diidentifikasi oleh application/vnd.font-fontforget-sfd sebagai tipe MIME-nya.

### Tajuk
Header file SFD yang umum adalah seperti yang ditunjukkan pada contoh berikut.

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


## **Referensi**

* [Format File SFD oleh FontForge](https://fontforge.org/docs/techref/sfdformat.html)

