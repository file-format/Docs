{
  "date": "2020-08-20",
  "keywords": [
"sdf-tiedosto",
"sdf-tiedostomuoto",
"mikä on sdf-tiedosto",
"tiedosto",
"sdf esimerkki",
"sdf tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SFD - Spline-fonttitietokantamuoto",
  "description": "Opi SFD-tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata SFD-tiedostoja.",
  "linktitle": "SFD",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-sf-fid"
}
},
  "lastmod": "2020-09-24"
}

## Mikä on SFD-tiedosto?

Tiedosto, jonka laajennus on .sfd (Spline Font Database), on natiivi ASCII-fonttimuoto fonttien muokkausohjelmistolle - FontForge. Ohjelmisto tukee monia muita yleisiä fonttimuotoja ja on vapaasti saatavilla. Ohjelmistoa voidaan käyttää lähes kaikissa nykyaikaisissa käyttöjärjestelmissä, mukaan lukien Linux, Windows ja MacOS.

## **SFD-tiedostomuoto**
SFD-tiedostot ovat ASCII-tiedostoja, jotka ovat ihmisen luettavissa ja joita on helppo siirtää Internetin kautta. Application/vnd.font-fontforget-sfd tunnistaa sen MIME-tyypiksi.

### Otsikko
Yleinen SFD-tiedoston otsikko on seuraavan esimerkin mukainen.

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


## **Referenssit**

 * [SFD File Format by FontForge](https://fontforge.org/docs/techref/sfdformat.html)

