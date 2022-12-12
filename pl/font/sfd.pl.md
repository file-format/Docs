{
  "date" : "2020-08-20",
  "keywords" :["plik sdf", "format pliku sdf", "co to jest plik sdf", "plik", "przykład sdf", "rozszerzenie pliku sdf", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - Format bazy danych czcionek splajnu",
  "description":"Dowiedz się o formacie pliku SFD i interfejsach API, które mogą tworzyć i otwierać pliki SFD.",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## Czym jest plik SDF?

Plik z rozszerzeniem .sfd (Spline Font Database) to natywny format czcionki ASCII dla oprogramowania do edycji czcionek - FontForge. Oprogramowanie obsługuje wiele innych popularnych formatów czcionek i jest ogólnodostępne. Oprogramowanie może być używane z prawie wszystkimi nowoczesnymi systemami operacyjnymi, w tym Linux, Windows i MacOS.

## **Format pliku SFD**
Pliki SFD to pliki ASCII, które są czytelne dla człowieka i można je łatwo przenosić przez Internet. Jest identyfikowany przez application/vnd.font-fontforget-sfd jako typ MIME.

### Nagłówek
Typowy nagłówek pliku SFD jest pokazany w poniższym przykładzie.

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


## **Bibliografia**

* [Format pliku SFD firmy FontForge](https://fontforge.org/docs/techref/sfdformat.html)

