
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - ไฟล์รหัสไบต์ ActionScript",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ ABC พร้อมตัวอย่างและ API ที่สามารถสร้างและเปิดไฟล์ ABC ได้",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## ไฟล์ ABC คืออะไร??

ไฟล์ที่มีนามสกุล .abc เป็นไฟล์รหัสไบต์ของ ActionScript ที่สร้างขึ้นโดยคอมไพเลอร์ Flash ซึ่งเป็นผลมาจากการคอมไพล์ไฟล์สคริปต์ ActionScript รหัสไบต์ที่มีอยู่ในไฟล์ ABC ดำเนินการโดย ActionScript Virtual Machine (AVM และ AVM2) รหัสไบต์ประกอบด้วยข้อมูลคงที่ คำสั่งจากชุดคำสั่ง AVM2 และข้อมูลเมตาประเภทต่างๆ เมื่อโหลดไฟล์ ABC ลงใน AVM หรือ AVM2 ไฟล์นั้นจะผ่านการตรวจสอบ หากไม่เป็นไปตามภาพรวม AVM2 จะถูกปฏิเสธ ไฟล์ ABC สามารถเปิดได้ใน Adobe Flash Player ที่เลิกผลิตไปนานแล้ว

## รูปแบบไฟล์ ABC - ข้อมูลเพิ่มเติม

ไฟล์ ABC ถูกบันทึกลงดิสก์ในรูปแบบไฟล์ไบนารีที่เครื่องเสมือน AVM หรือ AVM2 สามารถอ่านได้ โครงสร้างไฟล์ภายในแสดงถึงบล็อกโค้ดที่เรียกใช้งานได้พร้อมข้อมูลคงที่ ตัวอธิบายประเภท โค้ด และข้อมูลเมตาทั้งหมด

## โครงสร้างไฟล์ ABC

โครงสร้างไฟล์ ABC ดังภาพด้านล่าง

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### ฟิลด์ไฟล์ ABC

|ชื่อฟิลด์|คำอธิบาย|
---|---|
|minor_version, major_version|ค่าของ major_version และ minor_version คือหมายเลขเวอร์ชันหลักและรองของรูปแบบ abcFile|
|constant_pool|constant_pool คือโครงสร้างความยาวผันแปรที่ประกอบด้วยจำนวนเต็ม จำนวนคู่ สตริง เนมสเปซ ชุดเนมสเปซ และหลายชื่อ|
|method_count, method|ค่าของmethod_count คือจำนวนรายการในอาร์เรย์เมธอด แต่ละรายการในอาร์เรย์เมธอดคือโครงสร้าง method_info ที่มีความยาวผันแปรได้|
|metadata_count, metadata|ค่าของ metadata_count คือจำนวนรายการในอาร์เรย์ข้อมูลเมตา รายการข้อมูลเมตาแต่ละรายการคือ metadata_infostructure ที่แม็พชื่อกับชุดของค่าสตริง |
|class_count, อินสแตนซ์, คลาส| ค่าของ class_count คือจำนวนรายการในอินสแตนซ์และคลาสอาร์เรย์ |
|script_count, script|ค่าของ script_count คือจำนวนรายการในอาร์เรย์ของสคริปต์ แต่ละรายการสคริปต์เป็นโครงสร้าง script_info ที่กำหนดคุณลักษณะของสคริปต์เดียวในไฟล์นี้ |
|method_body_count, method_body|ค่าของ method_body_count คือจำนวนรายการในอาร์เรย์ method_body แต่ละ method_bodyentry ประกอบด้วยโครงสร้าง method_body_info ที่มีความยาวผันแปรได้ ซึ่งมีคำแนะนำสำหรับแต่ละเมธอดหรือฟังก์ชัน|

## อ้างอิง

* [ABC ที่แข็งแกร่ง (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

