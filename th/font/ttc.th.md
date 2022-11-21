{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - รูปแบบไฟล์คอลเลกชัน TrueType",
  "description":"ไฟล์ TrueType Collection (TTC) รวมฟอนต์หลายตัวไว้ในไฟล์เดียว ทั้ง Apple และ Microsoft ใช้ TTF บนระบบปฏิบัติการ Mac และ Windows",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## ไฟล์ TTC คืออะไร??
TTC ย่อมาจาก TrueType Collection เป็นส่วนเสริมของรูปแบบ True Type ไฟล์ TTC สามารถรวมไฟล์ฟอนต์หลายไฟล์เข้าด้วยกัน ไฟล์เหล่านี้มีประโยชน์สำหรับการรวมฟอนต์หลายตัวที่ใช้สัญลักษณ์หลายตัวร่วมกัน ก่อน Windows 2000 ไฟล์ TTC ถูกใช้ใน windows เวอร์ชันภาษาจีน ญี่ปุ่น และเกาหลี แต่ต่อมามีการสนับสนุนสำหรับทุกภูมิภาค


## โครงสร้างของไฟล์รวบรวมฟอนต์
ไฟล์ TTC ประกอบด้วยตาราง TTC Header, Table Directories และตาราง OpenType หลายตาราง ต้องพบส่วนหัว TTC ที่จุดเริ่มต้นของไฟล์ ต้องมีไดเร็กทอรีตารางที่สมบูรณ์สำหรับแต่ละฟอนต์ รูปแบบ TableDirectory ควรเหมือนกับที่มีอยู่ในไฟล์ที่ไม่ใช่คอลเลกชัน จำนวนตารางในไดเร็กทอรีทั้งหมดภายในไฟล์ TTC คำนวณจากจุดเริ่มต้นของไฟล์ TTC
ตารางในไฟล์ TTC ถูกอ้างอิงผ่านไดเร็กทอรีตารางของฟอนต์ที่เกี่ยวข้อง ตาราง OpenType บางตารางต้องแสดงหลายครั้ง หนึ่งครั้งสำหรับแต่ละฟอนต์ที่เพิ่มใน TTC ในขณะที่ตารางอื่นๆ อาจใช้ร่วมกันโดยแบบอักษรหลายตัวในไฟล์ TTC

### ส่วนหัว TTC
ตาราง TTC Header มีอยู่สองเวอร์ชัน:
- เวอร์ชัน 1.0 ใช้สำหรับไฟล์ TTC ที่ไม่มีลายเซ็นดิจิทัล
- สามารถใช้เวอร์ชัน 2.0 สำหรับไฟล์ TTC ที่มีหรือไม่มีลายเซ็นดิจิทัล
นี่คือตาราง TTC Header ของทั้งสองเวอร์ชัน:

**ส่วนหัว TTC เวอร์ชัน 1.0:**

|ประเภท|ชื่อ|คำอธิบาย|
---|---|---|
|TAG|ttcTag|สตริงรหัสคอลเลกชันแบบอักษร: 'ttcf' (ใช้สำหรับแบบอักษรที่มีโครงร่าง CFF หรือ CFF2 รวมถึงโครงร่าง TrueType)|
|uint16|majorVersion|เวอร์ชันหลักของ TTC Header, = 1.|
|uint16|minorVersion|เวอร์ชันรองของ TTC Header, = 0.|
|uint32|numFonts|จำนวนแบบอักษรใน TTC|
|Offset32|tableDirectoryOffsets[numFonts]|อาร์เรย์ออฟเซ็ตไปยัง TableDirectory สำหรับแต่ละฟอนต์จากจุดเริ่มต้นของไฟล์|

**ส่วนหัว TTC เวอร์ชัน 2.0:**

|ประเภท|ชื่อ|คำอธิบาย|
---|---|---|
|TAG|ttcTag |สตริงรหัสคอลเลกชันแบบอักษร: 'ttcf'|
|uint16| majorVersion | เวอร์ชันหลักของ TTC Header, = 2.|
|uint16| minorVersion | เวอร์ชันรองของ TTC Header, = 0.|
|uint32| numFonts | จำนวนแบบอักษรใน TTC|
|ออฟเซ็ต32| tableDirectoryOffsets[numFonts] |อาร์เรย์ออฟเซ็ตไปยัง TableDirectory สำหรับแต่ละฟอนต์จากจุดเริ่มต้นของไฟล์|
|uint32| dsigTag |แท็กระบุว่ามีตาราง DSIG อยู่ 0x44534947 ('DSIG') (null ถ้าไม่มีลายเซ็น)|
|uint32| dsigLength |ความยาว (เป็นไบต์) ของตาราง DSIG (null ถ้าไม่มีลายเซ็น)|
|uint32| dsigOffset |ออฟเซ็ต (เป็นไบต์) ของตาราง DSIG จากจุดเริ่มต้นของไฟล์ TTC (null หากไม่มีลายเซ็น)|

## อ้างอิง
* [ไฟล์แบบอักษร OpenType](https://docs.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (วิกิพีเดีย)](https://en.wikipedia.org/wiki/TrueType)

