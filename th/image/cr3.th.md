{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ CR3 - ไฟล์ภาพ Canon Raw 3",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CR3 และ API ที่สามารถสร้างและเปิดไฟล์ CR3",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## ไฟล์ CR3 คืออะไร??

ไฟล์ CR3 เป็นรูปแบบไฟล์ภาพ Canon RAW ที่สร้างขึ้นโดยกล้องดิจิตอล Canon บางรุ่น Canon นำมาใช้เพื่อแทนที่รูปแบบไฟล์ CR2 และถูกใช้โดยอุปกรณ์ดิจิทัลของ Canon บางรุ่น ไฟล์ CR3 เก็บข้อมูลภาพแบบไม่สูญเสียต้นฉบับที่กล้องถ่ายไว้ การใช้ภาพดิบเหล่านี้ทำให้ภาพมีคุณภาพสูงและช่วยให้ช่างภาพมีพื้นที่เหลือเฟือสำหรับการแก้ไข นอกจากข้อมูลรูปภาพหลักแล้ว ไฟล์ CR3 ยังเก็บข้อมูลเมตาดาต้าเกี่ยวกับรูปภาพด้วย

## รูปแบบไฟล์ CR3

ไฟล์ CR3 จัดเก็บลงดิสก์เป็นไฟล์ไบนารีในรูปแบบไฟล์สื่อฐาน ISO (ISO/IEC 14496-12) และยังมี [แท็ก Canon](https://exiftool.org/TagNames/Canon.html#uuid) ที่กำหนดเองด้วย นอกจากนี้ยังมี [ตัวแปลงสัญญาณ Canon 'crx'](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) ที่เป็นส่วนผสมของ JPEG-LS (Rice-Golomb + RLE การเข้ารหัส) และ JPEG-2000 (LeGall 5/3 DWT + การวัดปริมาณ)

## CR3 แท็กที่กำหนดเอง

ไฟล์ CR3 มีแท็กที่กำหนดเองสำหรับวัตถุประสงค์ที่แตกต่างกัน บางส่วนของแท็กเหล่านี้มีดังต่อไปนี้

|รหัสแท็ก| ชื่อแท็ก| เขียนได้ |ค่า / หมายเหตุ|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> แท็ก Canon CCTP|
|'CMT1' |IFD0| - |--> แท็ก EXIF|
|'CMT2' |ExifIFD| - |--> แท็ก EXIF|
|'CMT3' |MakerNoteCanon| - |--> แคนนอนแท็ก|
|'CMT4' |GPSInfo| - |--> แท็ก GPS|
|'CNCV' |เวอร์ชั่นคอมเพรสเซอร์| ไม่| |
|'CNOP' |CanonCNOP| - |--> แท็ก Canon CNOP|
|'CNTH' |CanonCNTH| - |--> แท็ก Canon CNTH|
|'THMB' |ภาพขนาดย่อ| ไม่| |

## อ้างอิง

* [รูปแบบไฟล์ CR2](http://lclevy.free.fr/cr2/)
* [แท็ก Canon](https://exiftool.org/TagNames/Canon.html#uuid)

