{
  "date" : "2020-08-20",
  "keywords" :[ "ไฟล์ sdf", "รูปแบบไฟล์ sdf", "ไฟล์ sdf คืออะไร", "ไฟล์", "ตัวอย่าง sdf", "นามสกุลไฟล์ sdf","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SFD - รูปแบบฐานข้อมูลแบบอักษร Spline",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ SFD และ API ที่สามารถสร้างและเปิดไฟล์ SFD",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## ไฟล์ SFD คืออะไร??

ไฟล์ที่มีนามสกุล .sfd (Spline Font Database) เป็นรูปแบบฟอนต์ ASCII ดั้งเดิมสำหรับซอฟต์แวร์แก้ไขฟอนต์ - FontForge ซอฟต์แวร์รองรับรองรับรูปแบบฟอนต์ทั่วไปอื่น ๆ และใช้งานได้ฟรี ซอฟต์แวร์นี้สามารถใช้ได้กับระบบปฏิบัติการสมัยใหม่เกือบทั้งหมด รวมทั้ง Linux, Windows และ MacOS

## **รูปแบบไฟล์ SFD**
ไฟล์ SFD เป็นไฟล์ ASCII ที่มนุษย์สามารถอ่านได้และถ่ายโอนผ่านอินเทอร์เน็ตได้อย่างง่ายดาย มีการระบุโดย application/vnd.font-fontforget-sfd เป็นประเภท MIME

### หัวข้อ
ส่วนหัวของไฟล์ SFD ทั่วไปแสดงอยู่ในตัวอย่างต่อไปนี้

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


## **ข้อมูลอ้างอิง**

* [รูปแบบไฟล์ SFD โดย FontForge](https://fontforge.org/docs/techref/sfdformat.html)

