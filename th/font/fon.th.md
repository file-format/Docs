{
  "date" : "2020-08-20",
  "keywords" :[ "ไฟล์ฟอน", "รูปแบบไฟล์ฟอน", "ไฟล์ฟอนคืออะไร", "ไฟล์", "ตัวอย่างฟอน", "นามสกุลไฟล์ฟอน", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - ไฟล์ไลบรารีแบบอักษร",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ FON และ API ที่สามารถสร้างและเปิดไฟล์ FON",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## ไฟล์ FON คืออะไร??

ไฟล์ที่มีนามสกุล .fon เป็นไลบรารีแบบอักษรของ Microsoft Windows 3.x ซึ่งเป็นไฟล์เรียกทำงานจริง แต่เปลี่ยนชื่อเป็น .fon เป็นชุดของไฟล์ [.fnt](/th/font/fnt/) ในตัวมันเอง และแอปพลิเคชันจะอ้างอิงถึงไฟล์ดังกล่าวในขณะที่เข้าถึงแบบอักษรของระบบ นั่นคือเหตุผลที่มันทำหน้าที่เป็นไฟล์ทรัพยากร สามารถเปิดได้บนระบบปฏิบัติการ Windows โดยใช้แอปพลิเคชัน Microsoft Windows Font View

## รูปแบบไฟล์ฟอน

ไฟล์ FON มีทรัพยากรแบบอักษรและมีรูปแบบไฟล์ทรัพยากร (.res) รูปแบบไฟล์ .res ระบุส่วนหัวของไฟล์ตลอดจนข้อมูลจำเพาะของส่วนข้อมูล นอกจากนี้ .fnt ยังเป็นไฟล์ข้อมูลทรัพยากรที่รวมอยู่ในไฟล์ทรัพยากรอีกด้วย ไฟล์ FON มีรูปแบบไฟล์ไบนารีและมีประเภท MIME ของแอปพลิเคชัน/ออคเต็ตสตรีม

ทรัพยากรฟอนต์ไม่เหมือนกับทรัพยากรประเภทอื่นๆ ที่ไม่ถูกเพิ่มไปยังทรัพยากรของแอปพลิเคชัน แต่จะถูกเพิ่มลงในไฟล์ EXE และเปลี่ยนชื่อเป็นไฟล์ .fon ส่งผลให้เป็นไฟล์ไลบรารีแทนแอปพลิเคชัน ฟอนต์ส่วนบุคคลหลายตัวประกอบด้วยส่วนประกอบของกลุ่มฟอนต์ที่แต่ละกลุ่มตามโครงสร้างกลุ่มรีซอร์ส ทรัพยากรฟอนต์ใช้โครงสร้างกลุ่มทรัพยากรเหล่านี้ ส่วนหัวของกลุ่มมีข้อมูลทั้งหมดที่จำเป็นในการเข้าถึงแบบอักษรเฉพาะจากกลุ่ม ทรัพยากรองค์ประกอบแบบอักษรมีรูปแบบดังต่อไปนี้
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/th/font/fnt/) file)
```
ไฟล์ทรัพยากร .rc ไฟล์เดียวสามารถมีการประกาศทรัพยากรแบบผสมได้ กลุ่มแบบอักษรสามารถอยู่ที่ใดก็ได้ในไฟล์ทรัพยากรและไม่จำเป็นต้องอยู่ติดกัน จำเป็นสำหรับโปรแกรมที่สร้างไฟล์ .RES เพื่อเพิ่มรายการด้วยตนเองของ FONTDIR ต่อไปนี้เป็นโครงสร้างของส่วนหัวของกลุ่ม

```
[ส่วนหัวของทรัพยากรปกติ (ประเภท = 7)]

คำจำนวนแบบอักษร; // จำนวนทั้งหมดในไฟล์ .RES
```     
The remaining data is repeated for every font in the .RES file.

```
WORD แบบอักษรOrdinal;
struct FontDirEntry {
Word รุ่น df;
DWORD dfSize;
ถ่าน dfCopyright [60];
WORD dfType;
คำ dfPoints;
คำ dfVertRes;
WORD dfHorizRes;
คำ dfAscent;
WORD dfInternalLeading;
คำ dfExternalLeading;
ไบต์ dfItalic;
BYTE dfขีดเส้นใต้;
ไบต์ dfStrikeOut;
WORD dfน้ำหนัก;
ไบต์ dfCharSet;
WORD dfPixWidth;
WORD dfPixHeight;
ไบต์ dfPitchAndFamily;
WORD dfAvgความกว้าง;
WORD dfMaxWidth;
ไบต์ dfFirstChar;
ไบต์ dfLastChar;
ไบต์ dfDefaultChar;
ไบต์ dfBreakChar;
WORD dfWidthBytes;
DWORD dfDevice;
DWORD dfFace;
DWORD dfReserved;
ถ่าน szDeviceName[];
ถ่าน szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

