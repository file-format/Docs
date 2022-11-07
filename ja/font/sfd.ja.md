{
  "date" : "2020-08-20",
  "keywords" :[ "sdf ファイル", "sdf ファイル形式", "sdf ファイルとは", "ファイル", "sdf の例", "sdf ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - スプライン フォント データベース形式",
  "description":"SFD ファイル形式と,SFD ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## .SFD オプション番号

拡張子が .sfd (Spline Font Database) のファイルは、フォント編集ソフトウェア - FontForge のネイティブ ASCII フォント形式です。このソフトウェアは、他の多くの一般的なフォント形式をサポートしており、自由に利用できます。このソフトウェアは、Linux、Windows、MacOS など、最新のほぼすべてのオペレーティング システムで使用できます。

## **SFD ファイル形式**
SFD ファイルは、人間が判読できる ASCII ファイルであり、インターネット経由で簡単に転送できます。 application/vnd.font-fontforget-sfd によって MIME タイプとして識別されます。

### ヘッダー
一般的な SFD ファイルのヘッダーは、次の例に示すとおりです。

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


## **参考文献**

* [FontForge による SFD ファイル形式](https://fontforge.org/docs/techref/sfdformat.html)

