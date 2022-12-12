{
  "date" : "2020-08-20",
  "keywords" :[ "fișier sdf", "format fișier sdf", "ce este un fișier sdf", "fișier", "exemplu sdf", "extensie fișier sdf", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - Format de bază de date fonturi Spline",
  "description":"Aflați despre formatul de fișier SFD și despre API-urile care pot crea și deschide fișiere SFD.",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## Ce este un fișier SFD?

Un fișier cu extensia .sfd (Spline Font Database) este formatul nativ de font ASCII pentru software-ul de editare a fonturilor - FontForge. Software-ul acceptă suportă multe alte formate comune de fonturi și este disponibil gratuit. Software-ul poate fi folosit pentru aproape toate sistemele de operare moderne, inclusiv Linux, Windows și MacOS.

## **Format de fișier SFD**
Fișierele SFD sunt fișiere ASCII care pot fi citite de om și sunt ușor de transferat pe internet. Este identificat prin application/vnd.font-fontforget-sfd ca tipul său MIME.

### Antet
Un antet comun al fișierului SFD este așa cum se arată în exemplul următor.

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


## **Referințe**

* [Format de fișier SFD de FontForge](https://fontforge.org/docs/techref/sfdformat.html)

