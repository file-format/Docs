{
  "date" : "2020-08-20",
  "keywords" :[ "sdf файл", "sdf файлов формат", "какво е sdf файл", "файл", "sdf пример", "sdf файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD – Формат на база данни с сплайн шрифтове",
  "description":"Научете за SFD файловия формат и API, които могат да създават и отварят SFD файлове.",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## Какво е SFD файл?

Файл с разширение .sfd (Spline Font Database) е основен ASCII шрифтов формат за софтуер за редактиране на шрифтове - FontForge. Софтуерът поддържа много други често срещани формати на шрифтове и е свободно достъпен. Софтуерът може да се използва за почти всички съвременни операционни системи, включително Linux, Windows и MacOS.

## **SFD файлов формат**
SFD файловете са ASCII файлове, които могат да се четат от хора и лесно се прехвърлят в интернет. Той се идентифицира от application/vnd.font-fontforget-sfd като свой MIME тип.

### Заглавие
Общата заглавка на SFD файл е както е показано в следния пример.

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


## **Препратки**

* [SFD файлов формат от FontForge](https://fontforge.org/docs/techref/sfdformat.html)

