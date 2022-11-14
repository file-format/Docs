{
  "date" : "2020-08-20",
  "keywords" :[ "fichier sdf", "format de fichier sdf", "qu'est-ce qu'un fichier sdf", "fichier", "exemple sdf", "extension de fichier sdf","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - Format de base de données de polices Spline",
  "description":"En savoir plus sur le format de fichier SFD et les API qui peuvent créer et ouvrir des fichiers SFD.",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## Qu'est-ce qu'un fichier SFD ?

Un fichier avec l'extension .sfd (Spline Font Database) est un format de police ASCII natif pour le logiciel d'édition de polices - FontForge. Le logiciel prend en charge de nombreux autres formats de police courants et est disponible gratuitement. Le logiciel peut être utilisé pour presque tous les systèmes d'exploitation modernes, y compris Linux, Windows et MacOS.

## **Format de fichier SFD**
Les fichiers SFD sont des fichiers ASCII lisibles par l'homme et facilement transférables sur Internet. Il est identifié par application/vnd.font-fontforget-sfd comme son type MIME.

### Entête
Un en-tête de fichier SFD commun est illustré dans l'exemple suivant.

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


## **Références**

* [Format de fichier SFD par FontForge] (https://fontforge.org/docs/techref/sfdformat.html)

