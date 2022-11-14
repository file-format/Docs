{
  "date" : "2020-08-20",
  "keywords" :[ "sdf-bestand", "sdf-bestandsformaat", "wat is een sdf-bestand", "bestand", "sdf-voorbeeld", "sdf-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - Spline Font Database Format",
  "description":"Meer informatie over SFD-bestandsindeling en API's die SFD-bestanden kunnen maken en openen.",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## Wat is een SFD-bestand?

Een bestand met de extensie .sfd (Spline Font Database) is een native ASCII-lettertypeformaat voor software voor het bewerken van lettertypen - FontForge. De software ondersteunt vele andere veelgebruikte lettertype-indelingen en is gratis beschikbaar. De software kan worden gebruikt voor bijna alle moderne besturingssystemen, waaronder Linux, Windows en MacOS.

## **SFD-bestandsindeling**
SFD-bestanden zijn ASCII-bestanden die voor mensen leesbaar zijn en gemakkelijk via internet kunnen worden overgedragen. Het wordt geïdentificeerd door application/vnd.font-fontforget-sfd als het MIME-type.

### Koptekst
Een algemene SFD-bestandsheader is zoals in het volgende voorbeeld wordt getoond.

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


## **Referenties**

* [SFD-bestandsindeling door FontForge](https://fontforge.org/docs/techref/sfdformat.html)

