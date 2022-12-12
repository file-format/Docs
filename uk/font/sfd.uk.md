{
  "date" : "2020-08-20",
  "keywords" :[ "файл sdf", "формат файлу sdf", "що таке файл sdf", "файл", "приклад sdf", "розширення файлу sdf", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - формат бази даних сплайнових шрифтів",
  "description":"Дізнайтеся про формат файлу SFD та API, які можуть створювати та відкривати файли SFD.",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## Що таке файл SFD?

Файл із розширенням .sfd (база даних сплайнових шрифтів) є рідним форматом шрифту ASCII для програмного забезпечення для редагування шрифтів – FontForge. Програмне забезпечення підтримує багато інших поширених форматів шрифтів і є у вільному доступі. Програмне забезпечення можна використовувати майже для всіх сучасних операційних систем, включаючи Linux, Windows і MacOS.

## **Формат файлу SFD**
Файли SFD – це файли ASCII, які легко читаються людиною та легко передаються через Інтернет. Його ідентифікує application/vnd.font-fontforget-sfd як тип MIME.

### Заголовок
Загальний заголовок файлу SFD, як показано в наступному прикладі.

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


## **Посилання**

* [Формат файлу SFD від FontForge](https://fontforge.org/docs/techref/sfdformat.html)

