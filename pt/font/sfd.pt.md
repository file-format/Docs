{
  "date" : "2020-08-20",
  "keywords" :[ "arquivo sdf", "formato de arquivo sdf", "o que é um arquivo sdf", "arquivo", "exemplo sdf", "extensão de arquivo sdf", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - Formato de banco de dados de fontes Spline",
  "description":"Saiba mais sobre o formato de arquivo SFD e APIs que podem criar e abrir arquivos SFD.",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## O que é um arquivo SFD?

Um arquivo com extensão .sfd (Spline Font Database) é um formato de fonte ASCII nativo para software de edição de fontes - FontForge. O software suporta muitos outros formatos de fonte comuns e está disponível gratuitamente. O software pode ser usado para quase todos os sistemas operacionais modernos, incluindo Linux, Windows e MacOS.

## **Formato de arquivo SFD**
Os arquivos SFD são arquivos ASCII legíveis por humanos e são facilmente transferidos pela Internet. Ele é identificado por application/vnd.font-fontforget-sfd como seu tipo MIME.

### Cabeçalho
Um cabeçalho de arquivo SFD comum é mostrado no exemplo a seguir.

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


## **Referências**

* [Formato de arquivo SFD por FontForge](https://fontforge.org/docs/techref/sfdformat.html)

