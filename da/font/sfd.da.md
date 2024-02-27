{
  "date": "2020-08-20",
  "keywords": [
"sdf-fil",
"sdf filformat",
"hvad er en sdf-fil",
"fil",
"sdf eksempel",
"sdf filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SFD - Spline Font Database Format",
  "description": "Lær om SFD-filformat og API'er, der kan oprette og åbne SFD-filer.",
  "linktitle": "SFD",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-sf-dad"
}
},
  "lastmod": "2020-09-24"
}

## Hvad er en SFD fil?

En fil med filtypenavnet .sfd (Spline Font Database) er et oprindeligt ASCII-skrifttypeformat til skrifttyperedigeringssoftware - FontForge. Softwaren understøtter understøtter mange andre almindelige skrifttypeformater og er frit tilgængelig. Softwaren kan bruges til næsten alle moderne operativsystemer inklusive Linux, Windows og MacOS.

## **SFD-filformat**
SFD-filer er ASCII-filer, der kan læses af mennesker, og som nemt kan overføres på tværs af internettet. Den identificeres af application/vnd.font-fontforget-sfd som dens MIME-type.

### Header
En almindelig SFD-filoverskrift er som vist i følgende eksempel.

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


## **Referencer**

 * [SFD File Format by FontForge](https://fontforge.org/docs/techref/sfdformat.html)

