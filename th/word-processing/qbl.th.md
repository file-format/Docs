{
  "date" : "2021-07-28",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QBL - ไฟล์ลิขสิทธิ์ QuickBooks",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ QBL และ API ที่สามารถสร้างและเปิดไฟล์ QBL",
  "linktitle" : "QBL",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-28"
}

## ไฟล์ QBL คืออะไร??

ไฟล์ที่มีนามสกุล .qbl คือไฟล์ใบอนุญาต QuickBooks ที่มีข้อมูลใบอนุญาตสำหรับสำเนาที่ผู้ใช้ซื้อ โดยปกติจะถูกจัดเก็บไว้ในระบบโลคัลโดยใช้ชื่อ `license.qbl` หลังจากติดตั้ง QuickBooks และผู้ใช้ป้อนข้อมูลสิทธิ์ใช้งานในซอฟต์แวร์เมื่อซอฟต์แวร์ถูกเรียกใช้เป็นครั้งแรก QBL เป็นรูปแบบไฟล์ก่อนหน้านี้ที่ใช้สำหรับจัดเก็บข้อมูลสิทธิ์การใช้งาน QuickBooks ตอนนี้สิ่งนี้ถูกแทนที่ด้วยไฟล์ QuickBooks `qbregisteration.dat` และเต็มไปด้วยข้อมูลจากอีเมลยืนยันของผู้ใช้ ดีวีดีที่ซื้อ หรือผ่านวิธีการซื้ออื่นๆ ไฟล์ QBL สามารถเปิดได้ในโปรแกรมแก้ไขข้อความใดๆ เช่น Windows Notepad, Apple TextEdit, Notepad++, Github Atom editor และอื่นๆ อีกมากมาย

## รูปแบบไฟล์ QBL - ข้อมูลเพิ่มเติม

ไฟล์ QBL ถูกสร้างขึ้นและจัดเก็บเป็นไฟล์ข้อความล้วน ข้อมูลในไฟล์เหล่านี้มนุษย์สามารถอ่านได้และสามารถแก้ไข/อัปเดตได้เมื่อเปิดไฟล์เหล่านี้ในโปรแกรมแก้ไขข้อความ จากนั้นสามารถคัดลอกข้อมูลสิทธิ์การใช้งานและการลงทะเบียนผู้ใช้ในไฟล์นี้เพื่อเริ่มต้นใช้งานซอฟต์แวร์ QuickBooks ไฟล์ QBL มักจะถูกเก็บไว้ในไดเร็กทอรี Program Files\Intuit\QuickBooks\INET บนระบบปฏิบัติการ Windows

ไฟล์ QBL มีข้อมูลสองประเภท

* `ข้อมูลเวอร์ชัน QuickBooks:` อ้างถึงเวอร์ชันที่ติดตั้งของ QuickBooks และอยู่ในรูปแบบเช่น xx.x
* `License Key:` ข้อความในรูปแบบ 000-000 0000-0000-0000-000 000073adbf3f โดยที่ 000-000 0000-0000-0000-000 ถูกแทนที่ด้วยรหัส qbregisteration ของผู้ใช้

## อ้างอิง

* [QuickBooks โดย Intuit](https://quickbooks.intuit.com/)
* [QuickBooks - การสร้างไฟล์ qbregistration.dat](https://quickbooks.intuit.com/learn-support/en-us/license-information/create-or-re-create-the-qbregistration-dat-file/ 00/186082)

