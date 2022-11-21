{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "ไฟล์", "นามสกุล", "รูปแบบไฟล์", "Excel", "สเปรดชีต" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ OTS และ API ที่สามารถสร้างและเปิดไฟล์ OTS",
  "title" :"OTS - รูปแบบไฟล์เทมเพลตสเปรดชีต OpenDocument",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## ไฟล์ OTS คืออะไร??

ไฟล์ที่มีนามสกุล .ots คือไฟล์เทมเพลตสเปรดชีต OpenDocument ที่สร้างขึ้นด้วยซอฟต์แวร์แอปพลิเคชัน Calc ที่รวมอยู่ใน Apache OpenOffice ซอฟต์แวร์แอปพลิเคชันการคำนวณคล้ายกับ Excel ที่มีใน Microsoft Office รูปแบบไฟล์ OTS ใช้เพื่อสร้างแม่แบบที่มีการตั้งค่าที่กำหนดไว้ล่วงหน้าเกี่ยวกับสไตล์ แบบอักษร ข้อมูล เค้าโครงสเปรดชีต และการจัดรูปแบบ ไฟล์ OTF มี `แอปพลิเคชันประเภทใบ้/vnd.oasis.opendocument.spreadsheet-template' ไฟล์เทมเพลตเหล่านี้สามารถใช้เป็นจุดเริ่มต้นในการสร้างและบันทึกไฟล์ข้อมูลจริงที่บันทึกไว้ใน [รูปแบบไฟล์ ODS](/th/spreadsheet/ods/) ไฟล์ OTS สามารถใช้กับแอปพลิเคชันเช่น OpenOffice และ LibreOffice

## รูปแบบไฟล์ OTS

ไฟล์ OTS ถูกบันทึกในรูปแบบไฟล์ OpenDocument XML ของ OASIS ซึ่งประกอบด้วยชุดเอกสารย่อยหลายชุดพร้อมแพ็คเกจเป็นไฟล์เก็บถาวร [ZIP](/th/compression/zip/) ไฟล์ zip แต่ละไฟล์จัดเก็บส่วนหนึ่งของเอกสารฉบับสมบูรณ์ และเอกสารย่อยแต่ละรายการจะจัดเก็บลักษณะเฉพาะของเอกสาร ตัวอย่างเช่น เอกสารย่อยหนึ่งประกอบด้วยข้อมูลลักษณะ และเอกสารย่อยอื่นประกอบด้วยเนื้อหาของเอกสาร เอกสาร ODF ทั่วไปมีองค์ประกอบดังต่อไปนี้:

### OTS Content.xml

ไฟล์ content.xml มีเนื้อหาจริงของเอกสาร ซึ่งไม่รวมถึงข้อมูลไบนารี เช่น รูปภาพ
```
<text:h style-name="Heading_2">This is a title</text:h>,
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### รูปแบบไฟล์ Styles.xml OTS

ไฟล์ style.xml มีข้อมูลการจัดรูปแบบและมีการใช้อย่างมากสำหรับการจัดรูปแบบและเค้าโครง ประเภทสไตล์ประกอบด้วย:

* รูปแบบย่อหน้า
* รูปแบบหน้า
* สไตล์ตัวละคร
* รูปแบบกรอบ
* รูปแบบรายการ

### เมตา.xml

ไฟล์ meta.xml มีข้อมูลเกี่ยวกับข้อมูลเมตาของไฟล์ เช่น ผู้แต่ง วันที่แก้ไขล่าสุด เป็นต้น
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### การตั้งค่า.xml

ไฟล์ `settings.xml` มีการตั้งค่าระดับเอกสาร เช่น ปัจจัยการซูมและตำแหน่งเคอร์เซอร์

## อ้างอิง ##

* [ข้อกำหนด OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - โดย Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

