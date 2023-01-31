{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - ภาษาข้อกำหนดของรายงานฝั่งไคลเอ็นต์",
  "keywords" :[ "rdlc", "ภาษาข้อกำหนดของรายงาน", "รูปแบบ mkv", "XSD", "ฝั่งไคลเอ็นต์ของข้อกำหนดของรายงาน"],
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ RDLC ซึ่งเป็นตัวแทน XML ของข้อกำหนดรายงาน SQL Server Reporting Services",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## ไฟล์ RDLC คืออะไร?? ##

RDLC ย่อมาจากฝั่งไคลเอ็นต์ภาษาข้อกำหนดของรายงาน ที่จริงแล้วเป็นส่วนขยายของไฟล์รายงานที่สร้างขึ้นโดยใช้เทคโนโลยีการรายงานของ Microsoft ตัวออกแบบรายงานเวอร์ชัน SQL Server 2005 ใช้เพื่อสร้างไฟล์เหล่านี้ การควบคุม **ReportViewer** ในฝั่งไคลเอ็นต์สามารถดำเนินการรายงาน RDLC ได้โดยตรง

## ไฟล์ RDL VS RDLC
|.rdl ไฟล์ |.rdlc ไฟล์|
---|---|
|ไฟล์ RDL ถูกสร้างขึ้นโดย Report Designer เวอร์ชัน SQL Server 2005|ไฟล์ RDLC ถูกสร้างขึ้นโดย Report Designer เวอร์ชัน Visual Studio 2005|
|มันถูกใช้ใน SQL Server Reporting Services|มันถูกใช้ใน Visual Studio|
|เป็นรายงานระยะไกล|เป็นรายงานในเครื่อง|
|ต้องการอินสแตนซ์ของ Reporting Services เพื่อเรียกใช้งาน|ไม่จำเป็นต้องมีอินสแตนซ์ของ Reporting Services|

## การสร้างไฟล์ข้อกำหนดรายงานลูกค้า (.rdlc)
ตัวควบคุม ReportViewer ใช้เพื่อรันไฟล์ข้อกำหนดรายงานไคลเอ็นต์ (.rdlc) โดยใช้ความสามารถในการประมวลผลในตัวของตัวควบคุม รายงานไคลเอนต์ที่คุณเรียกใช้ในโหมดการประมวลผลในเครื่องสามารถสร้างได้อย่างง่ายดายในโครงการแอปพลิเคชันของคุณ แนวทางการสร้างรายงานมีดังต่อไปนี้

- ใช้ **ตัวช่วยสร้างรายงาน** เพื่อสร้างคำนิยามรายงานไคลเอ็นต์ใหม่ (.rdlc)

- สร้างไฟล์ข้อกำหนดรายงานลูกค้าใหม่ (.rdlc) โดยใช้ Visual Studio

- สร้างข้อกำหนดของรายงานโดยทางโปรแกรม


คุณสามารถดูตัวอย่างรายงานได้โดยเรียกใช้ในการควบคุม **ReportViewer** เท่านั้น โปรดทราบว่าคุณสามารถเปิดและแก้ไขข้อกำหนดของรายงานได้ตลอดเวลา จากนั้นสร้างหรือปรับใช้แอปพลิเคชันเพื่อตรวจสอบผลลัพธ์

## อ้างอิง ##

- [การสร้างไฟล์ข้อกำหนดรายงานลูกค้า (.rdlc)](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))
