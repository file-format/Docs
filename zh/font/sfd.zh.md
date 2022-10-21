{
  "date" : "2020-08-20",
  "keywords" :["sdf 文件","sdf 文件格式","什么是 sdf 文件","文件","sdf 示例","sdf 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - 样条字体数据库格式",
  "description":"了解 SFD 文件格式和可创建和打开 SFD 文件的 API。",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## 什么是一 .sfd 文件？

扩展名为 .sfd（样条字体数据库）的文件是字体编辑软件 - FontForge 的原生 ASCII 字体格式。该软件支持许多其他常见的字体格式，并且是免费提供的。该软件可用于几乎所有现代操作系统，包括 Linux、Windows 和 MacOS。

## **SFD 文件格式**
SFD 文件是人类可读的 ASCII 文件，可轻松通过 Internet 传输。它由 application/vnd.font-fontforget-sfd 标识为其 MIME 类型。

### 标题
常见的 SFD 文件头如下例所示。

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


## **参考**

* [FontForge 的 SFD 文件格式](https://fontforge.org/docs/techref/sfdformat.html)

