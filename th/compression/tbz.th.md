{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ tbz", "รูปแบบไฟล์ tbz", "ไฟล์ tbz คืออะไร", "ไฟล์", "ตัวอย่าง tbz", "นามสกุลไฟล์ tbz","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - ไฟล์บีบอัด Bzip Tar",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ TBZ และ API ที่สามารถสร้างและเปิดไฟล์ TBZ",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## ไฟล์ TBZ คืออะไร??

ไฟล์ที่มีนามสกุล .tbz เป็นไฟล์เก็บถาวรแบบบีบอัดที่ใช้การบีบอัด BZIP เพื่อลดขนาดของไฟล์เนื้อหา ไฟล์ TBZ เป็นไฟล์เก็บถาวร UNIX [TAR](/th/compression/tar/) ที่ถูกบีบอัดด้วย BZIP การบีบอัดระดับที่สองล่าสุดคือ [BZIP2](/th/compression/bz2/) ที่มาแทนที่ BZIP รูปแบบไฟล์ TBZ เหมาะสำหรับการถ่ายโอนไฟล์ขนาดใหญ่ ไฟล์ TBZ สามารถเปิด/แตกไฟล์ได้โดยใช้แอปพลิเคชันซอฟต์แวร์ เช่น 7-Zip, PeaZip และ jZip ผู้ใช้ Linux และ macOS ยังสามารถเปิด TBZ ด้วยคำสั่ง BZIP2 จากหน้าต่างเทอร์มินัล

## รูปแบบไฟล์ TBZ

ไฟล์ TBZ เป็นไฟล์บีบอัดที่สร้างขึ้นด้วยการบีบอัด BZIP/[BZIP2](/th/compression/bz2) ไม่มีข้อกำหนดอย่างเป็นทางการสำหรับรูปแบบไฟล์นี้ อย่างไรก็ตาม [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) อย่างไม่เป็นทางการแสดงว่าสตรีม .bz2 ประกอบด้วยส่วนหัว 4 ไบต์ซึ่งตามมาด้วย โดยบล็อกบีบอัดเป็นศูนย์หรือมากกว่า

## อ้างอิง ##

* [ข้อกำหนดรูปแบบ BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

