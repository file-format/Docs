{
  "date" : "2022-06-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ GZIP - ไฟล์เก็บถาวรซิป GNU",
  "description":"เรียนรู้เกี่ยวกับไฟล์ GZIP และ API ที่สามารถสร้างและเปิดไฟล์ GZIP ได้",
  "linktitle" : "GZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-26"
}

## ไฟล์ GZIP คืออะไร??

ไฟล์ GZIP เป็นไฟล์เก็บถาวรแบบบีบอัดที่สร้างขึ้นด้วยอัลกอริธึมการบีบอัดมาตรฐาน [gzip] (https://en.wikipedia.org/wiki/Gzip) (GNU zip) ไฟล์เก็บถาวรแบบบีบอัดอาจมีไฟล์หลายไฟล์ รวมถึงไฟล์บีบอัด ไดเร็กทอรี และต้นขั้วไฟล์ ระบบ Unix ส่วนใหญ่มียูทิลิตี้บีบอัด gzip (GNU Zip) แบบโอเพ่นซอร์สสำหรับการบีบอัด/คลายการบีบอัดไฟล์ ไฟล์ GZIP สามารถเปิดได้ด้วยแอปพลิเคชัน เช่น [WinZip](https://www.winzip.com/en/)

## รูปแบบไฟล์ GZIP - ข้อมูลเพิ่มเติม

GZIP ใช้อัลกอริทึม [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) เพื่อบีบอัดไฟล์เป็นไฟล์เก็บถาวร RFC สองตัว, [RFC1952](https://tools.ietf.org/html/rfc1952) และ [RFC 1951](https://tools.ietf.org/html/rfc1951) กำหนดข้อกำหนดของรูปแบบตัวตัดคำ gzip และยุบรูปแบบข้อมูลที่บีบอัดตามลำดับ

ไฟล์ GZIP มักจะบันทึกเป็นรูปแบบไฟล์ [GZ](/th/compression/gz/)

## อ้างอิง

* [gzip](http://www.gzip.org/)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: ข้อกำหนดรูปแบบไฟล์ GZIP](http://tools.ietf.org/html/rfc1952) โดย IETF
* [RFC 1951](https://tools.ietf.org/html/rfc1951)

