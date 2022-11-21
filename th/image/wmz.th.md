{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ wmz", "รูปแบบไฟล์ wmz", "ไฟล์ wmz คืออะไร", "ไฟล์", "ตัวอย่าง wmz", "นามสกุลไฟล์ wmz","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ WMZ - Windows Metafile ที่บีบอัด",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ WMZ และ API ที่สามารถสร้างและเปิดไฟล์ WMZ",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## ไฟล์ WMZ คืออะไร??

ไฟล์ที่มีนามสกุล .wmz เป็นเวอร์ชันบีบอัดของ [WMF](/th/image/wmf/) และใช้เพื่อจัดเก็บไฟล์เมตา เป็นไฟล์ระดับกลางที่สร้างโดยแอปพลิเคชัน Microsoft Office เวอร์ชันเก่าและไม่เป็นที่นิยมใช้มากนัก ไฟล์ WMZ จะถูกสร้างขึ้นในขณะที่บันทึกเอกสารเป็นรูปแบบ [HTML](/th/web/html/) สิ่งเหล่านี้อาจถูกสร้างขึ้นในขณะที่ส่งอีเมลเอกสารที่มีคลิปอาร์ตฝังตัว สมการ ฯลฯ แอปพลิเคชันที่สามารถเปิดไฟล์ WMZ รวมถึง (แต่ไม่จำกัดเฉพาะ) Corel Winzip และ Apple Archive Utility

## รูปแบบไฟล์ WMZ

ไฟล์ WMZ ถูกบีบอัดแบบ [Gzip](/th/compression/gz/) และมี [WMF](/th/image/WMF/) อยู่ภายใน Gzip ใช้อัลกอริธึม DEFLATE สำหรับการบีบอัดไฟล์เก็บถาวร GZIP แตกต่างจากรูปแบบไฟล์เก็บถาวร [ZIP](/th/compression/zip/) เนื่องจากใช้อัลกอริทึมการบีบอัดเพื่อทำให้ไฟล์เก็บถาวรสมบูรณ์แทนที่จะเป็นไฟล์แต่ละไฟล์ รูปแบบไฟล์ประกอบด้วย:

* ส่วนหัวของไฟล์
* ส่วนหัวเสริม
* ข้อมูลที่บีบอัด
* ส่วนท้ายของไฟล์

รูปแบบไฟล์ GZIP [ข้อมูลจำเพาะเวอร์ชัน 4.3](http://tools.ietf.org/html/rfc1952) ที่เผยแพร่โดย Internet Engineering Task Force (IETF) มีข้อมูลโดยละเอียดเกี่ยวกับรูปแบบไฟล์

## อ้างอิง

* [RFC1952: ข้อกำหนดรูปแบบไฟล์ GZIP](http://tools.ietf.org/html/rfc1952) โดย [IETF](https://ietf.org)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

