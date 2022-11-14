{
  "date" : "2020-08-20",
  "keywords" :[ "sdf 파일", "sdf 파일 형식", "sdf 파일이란", "파일", "sdf 예제", "sdf 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - 스플라인 글꼴 데이터베이스 형식",
  "description":"SFD 파일 형식과 SFD 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## .SFD 파일이란?

.sfd(Spline Font Database) 확장자를 가진 파일은 글꼴 편집 소프트웨어인 FontForge의 기본 ASCII 글꼴 형식입니다. 이 소프트웨어는 다른 많은 일반 글꼴 형식을 지원하며 무료로 사용할 수 있습니다. 이 소프트웨어는 Linux, Windows 및 MacOS를 포함한 거의 모든 최신 운영 체제에서 사용할 수 있습니다.

## **SFD 파일 형식**
SFD 파일은 사람이 읽을 수 있고 인터넷을 통해 쉽게 전송할 수 있는 ASCII 파일입니다. MIME 유형으로 application/vnd.font-fontforget-sfd에 의해 식별됩니다.

### 헤더
일반적인 SFD 파일 헤더는 다음 예와 같습니다.

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


## **참고문헌**

* [FontForge의 SFD 파일 형식](https://fontforge.org/docs/techref/sfdformat.html)

