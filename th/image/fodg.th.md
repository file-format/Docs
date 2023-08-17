{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ fodg", "รูปแบบไฟล์ fodg", "ไฟล์ fodg คืออะไร", "ไฟล์", "ตัวอย่าง fodg", "นามสกุลไฟล์ fodg", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - รูปแบบไฟล์การวาด OpenDocument",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ FODG และ API ที่สามารถสร้างและเปิดไฟล์ FODG",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ FODG คืออะไร??

ไฟล์ที่มีนามสกุล .fodg เป็นรูปแบบไฟล์ Apache OpenOffice Drawing สำหรับจัดเก็บองค์ประกอบรูปวาด โดยอิงตามข้อกำหนดรูปแบบไฟล์ที่ระบุโดย Advancement of Structural Information Standards (OASIS) รูปแบบไฟล์อื่นที่คล้ายกันสำหรับกราฟิก OpenOffice คือ [ODG](/th/image/odg/) ที่เก็บองค์ประกอบการวาดเป็นภาพเวกเตอร์ ไฟล์ FODG สามารถเปิดได้ด้วย OpenOffice และ LibreOffice รูปแบบไฟล์อื่นๆ ที่ OpenOffice รองรับ เช่น [ODT](/th/word-processing/odt/), ODF, [ODP](/th/presentation/odp/) และ [ODS](/th/spreadsheet/ods/)

## รูปแบบไฟล์ FODG

FODG ใช้รูปแบบไฟล์ XML ของ OpenDocument ที่สอดคล้องกับ OASIS OpenDocument Format ISO/IEC 26300 มี Internet Media Type application/vnd.oasis.opendocument.graphics และยังเป็นไปตาม org.oasis-open.opendocument public.composite-content . โครงสร้าง XML เป็นแบบทั่วไปสำหรับเอกสารทุกประเภท เช่น สเปรดชีต ไฟล์รูปวาด และเอกสารข้อความ เอกสาร OpenOffice ใช้ประโยชน์จากการแยกข้อกังวลโดยแยกเนื้อหา ลักษณะ ข้อมูลเมตา และการตั้งค่าแอปพลิเคชันออกเป็นไฟล์ XML สี่ไฟล์แยกกัน

`<office:document-content> ` - เนื้อหาเอกสารและรูปแบบอัตโนมัติที่ใช้ในเนื้อหา
`<office:document-styles> ` - สไตล์ที่ใช้ในเนื้อหาเอกสารและสไตล์อัตโนมัติที่ใช้ในสไตล์เอง
`<office:document-meta> ` - ข้อมูลเมตาของเอกสาร เช่น ผู้เขียนหรือเวลาของการดำเนินการบันทึกครั้งล่าสุด
`<office:document-settings> ` - การตั้งค่าเฉพาะแอปพลิเคชัน เช่น ขนาดหน้าต่างหรือข้อมูลเครื่องพิมพ์

## อ้างอิง ##
* [ข้อกำหนดในอนาคตสำหรับการกำหนดมาตรฐาน v 1.3 ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [รูปแบบเอกสาร OASIS Open สำหรับแอปพลิเคชัน Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [รูปแบบ OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

