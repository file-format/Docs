{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "extension", "file", "file format", "Database File Type", "Database File Format", "Btrieve Database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ BTR และ API ที่สามารถสร้างและเปิดไฟล์ BTR",
  "title" :"BTR - ไฟล์ฐานข้อมูล Btrieve",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## ไฟล์ BTR คืออะไร??

ไฟล์ที่มีนามสกุล .btr คือไฟล์ฐานข้อมูลที่สร้างโดยแอปพลิเคชันฐานข้อมูลธุรกรรม [Btrieve](https://www.actian.com/) ซึ่งแตกต่างจากระบบการจัดการฐานข้อมูลเชิงสัมพันธ์ (RBMS) Btrieve นั้นใช้ Indexed Sequential Access Method (ISAM) ซึ่งเป็นวิธีการจัดเก็บข้อมูลเพื่อการเรียกใช้ที่รวดเร็ว ไฟล์ BTR จัดเก็บชุดบันทึกและใช้เพื่อสร้างรายงานตามข้อกำหนด ไฟล์ BTR สามารถเปิดได้โดยใช้ Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility และ Legend Software BTRIEVE Viewer

## โครงสร้างไฟล์ BTR - ข้อมูลเพิ่มเติม

โครงสร้างข้อมูลภายในและการจัดตำแหน่งของแต่ละไบต์ในโครงสร้างของไฟล์ BTR ไม่เปิดเผยต่อสาธารณะ อย่างไรก็ตาม Btrieve
ให้ [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) ที่สามารถใช้เพื่ออ่านข้อมูลจากไฟล์ BTR เข้ากันได้กับภาษาการเขียนโปรแกรมและสภาพแวดล้อมการพัฒนาต่อไปนี้

* เอ็มบาร์คาเดโร C/C++
* เอ็มบาร์คาเดโร เดลฟี
* GNU C/C++
* ไมโครโฟกัสภาษาโคบอล
* ไมโครซอฟต์ Visual Basic
* ไมโครซอฟต์ Visual C++
* วัตคอม C/C++

การดึงข้อมูลจากไฟล์ BTR ขึ้นอยู่กับไฟล์ DDF ที่เกี่ยวข้อง หากไม่มี DDF การดึงข้อมูลจากไฟล์ดังกล่าวจะไม่ง่าย

## อ้างอิง

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [ข้อมูลเบื้องต้นเกี่ยวกับ Btreive API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

