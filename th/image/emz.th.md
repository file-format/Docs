{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ emz", "รูปแบบไฟล์ emz", "ไฟล์ emz คืออะไร", "ไฟล์", "ตัวอย่าง emz", "นามสกุลไฟล์ emz","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ EMZ - ไฟล์ Meta ที่ปรับปรุงแล้วของ Windows ที่บีบอัด",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ EMZ และ API ที่สามารถสร้างและเปิดไฟล์ EMZ",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## ไฟล์ EMZ คืออะไร??

ไฟล์ที่มีนามสกุล .emz เป็นคอนเทนเนอร์บีบอัดของไฟล์ Enhanced Metafile ([EMF](/th/image/emf/)) สิ่งเหล่านี้ถูกบีบอัดโดยใช้เทคนิคการบีบอัด [GZIP](/th/compression/gz/) ซึ่งเป็นวิธีการบีบอัดที่ใช้กันทั่วไปในระบบปฏิบัติการ UNIX และ LINUX ยกเลิกการเชื่อมโยง ZIP (/th/compression/zip/) GZIP จะบีบอัดไฟล์เก็บถาวรโดยรวมแทนที่จะบีบอัดทีละไฟล์ ไฟล์ EMZ มีขนาดเล็กกว่าเมื่อเทียบกับไฟล์ EMF และช่วยในการถ่ายโอนที่รวดเร็วระหว่างการแชร์ไฟล์ออนไลน์ แอปพลิเคชันบางตัวที่สามารถเปิดไฟล์ EMZ ได้แก่ Microsoft Visio 2019, Microsoft Office 2019, XnView MP และ File Viewer Plus

## รูปแบบไฟล์ EMZ

ไฟล์ EMZ ถูกบีบอัดแบบ [Gzip](/th/compression/gz/) และมี [EMF](/th/image/emf/) อยู่ภายใน Gzip ใช้อัลกอริทึม DEFLATE สำหรับการบีบอัดไฟล์เก็บถาวรและมีความแตกต่างในการใช้การบีบอัด ไฟล์ EMZ สามารถขยายได้โดยใช้ยูทิลิตี้การบีบอัด GZip เช่น GNU Zip รูปแบบไฟล์ประกอบด้วย:

* ส่วนหัวของไฟล์
* ส่วนหัวเสริม
* ข้อมูลที่บีบอัด
* ส่วนท้ายของไฟล์

รูปแบบไฟล์ GZIP [ข้อมูลจำเพาะเวอร์ชัน 4.3](https://datatracker.ietf.org/doc/html/rfc1952) ที่เผยแพร่โดย Internet Engineering Task Force (IETF) มีข้อมูลโดยละเอียดเกี่ยวกับรูปแบบไฟล์

## อ้างอิง

* [RFC1952: ข้อกำหนดรูปแบบไฟล์ GZIP](https://datatracker.ietf.org/doc/html/rfc1952) โดย [IETF](https://www.ietf.org/)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

