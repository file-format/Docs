{
  "date" : "2022-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ TRM และ API ที่สามารถสร้างและเปิดไฟล์ TRM",
  "title" :"รูปแบบไฟล์ TRM - ไฟล์ Oracle Trace Map",
  "linktitle" : "TRM",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## ไฟล์ Oracle TRM คืออะไร?

ไฟล์ TRM เป็นรูปแบบไฟล์ข้อมูลเมตาที่ใช้โดยระบบจัดการฐานข้อมูลเชิงสัมพันธ์ Oracle 11g (RDBMS) โดยจัดเก็บไว้ข้างไฟล์ Oracle Trace ([.trc](/th/database/trc/)) และมีข้อมูลโครงสร้างเกี่ยวกับไฟล์ติดตาม วัตถุประสงค์ของไฟล์ TRM คือเพื่ออำนวยความสะดวกในการค้นหาและนำทางบันทึกโดยใช้ข้อมูลเมตาดาต้า สามารถใช้ซอฟต์แวร์ Oracle เพื่อเปิดไฟล์ TRM

## รูปแบบไฟล์ TRM

ไฟล์ TRM ถูกบันทึกในรูปแบบไฟล์ที่เป็นกรรมสิทธิ์ของ Oracle และรายละเอียดรูปแบบไฟล์ TRM จะไม่เปิดเผยต่อสาธารณะ ไฟล์ TRC ทั่วไปประกอบด้วย Oracle process SID, ชื่อกระบวนการ และหมายเลขกระบวนการ OS ไฟล์ TRM มีข้อมูลเมตาโดยละเอียดเกี่ยวกับไฟล์ TRC เหล่านี้สำหรับการค้นหาและการนำทาง

## อ้างอิง ##

* [ไฟล์ .trm ใน oracle 11g คืออะไร](https://community.oracle.com/tech/developers/discussion/945615/what-is-trm-file-in-oracle-11g)
