{
  "date" : "2020-08-20",
  "keywords" :[ "файл sdf", "формат файла sdf", "что такое файл sdf", "файл", "пример sdf", "расширение файла sdf", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD — формат базы данных сплайновых шрифтов",
  "description":"Узнайте о формате файла SFD и API-интерфейсах, которые могут создавать и открывать файлы SFD.",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## .SFD вариант №

Файл с расширением .sfd (база данных шрифтов Spline) является собственным форматом шрифта ASCII для программного обеспечения для редактирования шрифтов — FontForge. Программное обеспечение поддерживает многие другие распространенные форматы шрифтов и находится в свободном доступе. Программное обеспечение можно использовать практически для всех современных операционных систем, включая Linux, Windows и MacOS.

## **Формат файла SFD**
Файлы SFD представляют собой файлы ASCII, которые удобочитаемы для человека и легко передаются через Интернет. Он идентифицируется application/vnd.font-fontforget-sfd как тип MIME.

### Заголовок
Общий заголовок файла SFD показан в следующем примере.

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


## **Использованная литература**

* [Формат файла SFD от FontForge] (https://fontforge.org/docs/techref/sfdformat.html)

