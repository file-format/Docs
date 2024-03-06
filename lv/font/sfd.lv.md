{
  "date": "2020-08-20",
  "keywords": [
"sdf failu",
"sdf faila formātā",
"kas ir sdf fails",
"failu",
"sdf piemērs",
"sdf faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SFD — Spline fontu datu bāzes formāts",
  "description": "Uzziniet par SFD faila formātu un API, kas var izveidot un atvērt SFD failus.",
  "linktitle": "SFD",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-sf-lvd"
}
},
  "lastmod": "2020-09-24"
}

## Kas ir SFD fails?

Fails ar paplašinājumu .sfd (Spline Font Database) ir vietējais ASCII fonta formāts fontu rediģēšanas programmatūrai — FontForge. Programmatūra atbalsta daudzus citus izplatītus fontu formātus un ir brīvi pieejama. Programmatūru var izmantot gandrīz visām mūsdienu operētājsistēmām, tostarp Linux, Windows un MacOS.

## **SFD faila formāts**
SFD faili ir ASCII faili, kas ir lasāmi cilvēkiem un ir viegli pārsūtīti pa internetu. Tas tiek identificēts ar application/vnd.font-fontforget-sfd kā MIME tipu.

### Galvene
Kopējā SFD faila galvene ir tāda, kā parādīts nākamajā piemērā.

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


## **Atsauces**

 * [SFD File Format by FontForge](https://fontforge.org/docs/techref/sfdformat.html)

