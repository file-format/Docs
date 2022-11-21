{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ FMPSL และ API ที่สามารถสร้างและเปิดไฟล์ FMPSL",
  "title" :"รูปแบบไฟล์ FMPSL - ไฟล์ลิงก์ Snapshot FileMaker Pro 12",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## ไฟล์ FMPSL คืออะไร??

ไฟล์ FMPSL เป็นไฟล์สแนปช็อตของฐานข้อมูลที่สร้างด้วย FileMaker Pro 12 โดยจะเก็บผลลัพธ์ที่สอบถามจากฐานข้อมูลพร้อมกับข้อมูลอื่นๆ เช่น เค้าโครงภาพและข้อมูลที่มองเห็นได้ ไฟล์ FMPSL สามารถใช้เพื่อกู้คืนข้อมูลทั้งหมดนี้ในอินสแตนซ์อื่นของฐานข้อมูล FileMaker Pro รูปแบบไฟล์นี้ถูกนำมาใช้พร้อมกับการเปิดตัว FileMaker Pro v 12 ก่อนเวอร์ชันนี้ ลิงก์สแน็ปช็อตได้รับการแนะนำเป็นรูปแบบไฟล์ FPSL ใน FileMaker Pro v 11 ไฟล์ FMPSL สามารถเปิดได้ด้วยซอฟต์แวร์ FileMaker Pro Advanced รูปแบบไฟล์อื่นๆ ที่ FileMaker Pro รองรับได้แก่ [FP5](/th/database/fp5/), [FP7](/th/database/fp7/) และ [FMP12](/th/database/fmp12/)

## รูปแบบไฟล์ FMPSL

รายละเอียดรูปแบบไฟล์ภายในของไฟล์ FMPSL ไม่เปิดเผยต่อสาธารณะสำหรับการอ้างอิงของผู้พัฒนา

### วิธีบันทึกบันทึกเป็นไฟล์ FMPSL

ข้อมูลจากฐานข้อมูล FileMaker Pro สามารถบันทึกเป็นไฟล์ลิงค์สแน็ปช็อตโดยใช้ขั้นตอนต่อไปนี้

1. ค้นหาบันทึกจากฐานข้อมูลที่ต้องการบันทึกเป็นไฟล์ลิงค์สแน็ปช็อต
1. ใช้ตัวเลือก Send Record As Snapshot Link จากเมนู บันทึกไฟล์โดยป้อนชื่อไฟล์
1. ใช้บันทึกที่กำลังเรียกดูเพื่อบันทึกชุดบันทึกที่พบทั้งหมด

ไฟล์สแน็ปช็อตที่สร้างขึ้นจะถูกบันทึกลงดิสก์ด้วยชื่อที่ระบุ

## อ้างอิง

* [แปลงรูปแบบไฟล์ FileMaker Pro เวอร์ชันก่อนหน้าเป็นรูปแบบไฟล์ FMP12](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [บันทึกเป็นไฟล์ลิงก์ Snapshot](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

