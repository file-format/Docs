{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "นามสกุล", "ไฟล์", "รูปแบบ", "eBook", "รูปแบบไฟล์ Kindle", "โครงสร้างไฟล์ AZW3" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ AZW3 และ API ที่สามารถสร้างและเปิดไฟล์ AZW3",
  "title" :"ไฟล์ AZW3 คืออะไร",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## ไฟล์ AZW3 คืออะไร??

AZW3 หรือที่เรียกว่า Kindle Format 8 (**KF8**) เป็นเวอร์ชันแก้ไขของรูปแบบไฟล์ดิจิทัล ebook [AZW](/th/ebook/azw/) ที่พัฒนาขึ้นสำหรับอุปกรณ์ Amazon Kindle รูปแบบนี้เป็นการเพิ่มประสิทธิภาพให้กับไฟล์ AZW รุ่นเก่า และใช้บนอุปกรณ์ Kindle Fire ที่มีความเข้ากันได้แบบย้อนหลังเท่านั้นสำหรับรูปแบบไฟล์ก่อนหน้า เช่น [MOBI](/th/ebook/mobi/) และ AZW Amazon เปิดตัวรูปแบบ KFX (KF เวอร์ชัน 10) หลังจาก KF8 ที่ใช้บนอุปกรณ์ Kindle รุ่นล่าสุด ไฟล์ AZW3 มีแอปพลิเคชันประเภทสื่ออินเทอร์เน็ต/vnd.amazon.mobi8-ebook ไฟล์ AZW3 สามารถแปลงเป็นไฟล์รูปแบบอื่นๆ ได้ เช่น [PDF](/th/pdf/), [EPUB](/th/ebook/epub/), [AZW](/th/ebook/azw/), [DOCX](/th/ การประมวลผลคำ/docx/) และ [RTF](/th/การประมวลผลคำ/rtf/)

## รูปแบบไฟล์ AZ3/KF8 ##

ไฟล์ KF8 มีลักษณะเป็นไบนารีและคงโครงสร้างของรูปแบบไฟล์ MOBI เป็นไฟล์ PDB ตามที่กล่าวไว้ก่อนหน้านี้ ไฟล์ KF8 อาจมีทั้ง MOBI และ EPUB เวอร์ชัน KF8 ที่ใหม่กว่าในภายหลัง รายละเอียดภายในของรูปแบบได้รับการถอดรหัสโดย [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack) ซึ่งเป็นสคริปต์ Python ที่แยกวิเคราะห์ฐานข้อมูลที่รวบรวมขั้นสุดท้ายและแยกไฟล์ต้นฉบับ MOBI หรือ AZW ไฟล์ AZW3 (KF8) มีเป้าหมายเป็นเวอร์ชัน EPUB3 ที่มีความเข้ากันได้แบบย้อนหลังสำหรับ EPUB เช่นกัน KF8 รวบรวมไฟล์ EPUB และสร้างโครงสร้างไบนารีตามรูปแบบไฟล์ PDB

## อ้างอิง ##

* [KF8 - โดย Wikipedia](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [แกะกล่อง Kindle](https://github.com/kevinhendricks/KindleUnpack)

