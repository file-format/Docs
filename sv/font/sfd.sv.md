{
  "date" : "2020-08-20",
  "keywords" :[ "sdf-fil", "sdf-filformat", "vad är en sdf-fil", "fil", "sdf-exempel", "sdf-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - Spline Font Database Format",
  "description":"Läs mer om SFD-filformat och API:er som kan skapa och öppna SFD-filer.",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## Vad är en SFD fil?

En fil med tillägget .sfd (Spline Font Database) är ett inbyggt ASCII-teckensnittsformat för teckensnittsredigeringsprogram - FontForge. Programvaran stöder stöder många andra vanliga teckensnittsformat och är fritt tillgänglig. Programvaran kan användas för nästan alla moderna operativsystem inklusive Linux, Windows och MacOS.

## **SFD-filformat**
SFD-filer är ASCII-filer som är läsbara för människor och som enkelt kan överföras över internet. Den identifieras av application/vnd.font-fontforget-sfd som dess MIME-typ.

### Rubrik
En vanlig SFD-filrubrik är som visas i följande exempel.

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


## **Referenser**

* [SFD-filformat av FontForge](https://fontforge.org/docs/techref/sfdformat.html)

