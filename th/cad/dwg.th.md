{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "รูปแบบไฟล์", "CAD", "เปิด", "สร้าง" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ DWG และ API ที่สามารถสร้างและเปิดไฟล์ DWG",
  "title" :"รูปแบบไฟล์ DWG",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ DWG คืออะไร??

ไฟล์ที่มีนามสกุล DWG แสดงถึงไฟล์ไบนารีที่เป็นกรรมสิทธิ์ซึ่งใช้สำหรับเก็บข้อมูลการออกแบบ 2D และ 3D เช่นเดียวกับ DXF ซึ่งเป็นไฟล์ ASCII DWG เป็นตัวแทนของรูปแบบไฟล์ไบนารีสำหรับการเขียนแบบ CAD (Computer Aided Design) ประกอบด้วยภาพเวกเตอร์และข้อมูลเมตาสำหรับการแสดงเนื้อหาของไฟล์ CAD มีโปรแกรมดูฟรีสำหรับการดูไฟล์ DWG บนระบบปฏิบัติการ Windows เช่น DWG TrueView ฟรีของ Autodesk มีแอปพลิเคชันบุคคลที่สามอื่น ๆ ที่รองรับการเข้าถึงไฟล์ DWG ไฟล์ DWG มีข้อมูลที่สร้างโดยผู้ใช้และรวมถึง:

* การออกแบบ
* ข้อมูลทางเรขาคณิต
* แผนที่และภาพถ่าย

รูปแบบนี้ใช้กันอย่างแพร่หลายโดยสถาปนิก วิศวกร และนักออกแบบเพื่อวัตถุประสงค์ในการออกแบบต่างๆ

## ประวัติย่อ ##

รูปแบบไฟล์ DWG ได้รับการพัฒนาตามเวลานับตั้งแต่มีการเปิดตัวอย่างเป็นทางการในปี 1982 ภาพรวมโดยย่อของเหตุการณ์ในอดีตจากมุมมองของประวัติศาสตร์มีดังต่อไปนี้

**1982:** Autodesk อนุญาตให้ใช้รูปแบบไฟล์ DWG ซึ่งพัฒนาโดย Mike Riddle ในปี 1970 เป็นพื้นฐานสำหรับ AutoCAD

**1998:** ด้วยการเปิดตัว AutoCAD R14.01 Autodesk ได้เพิ่มการตรวจสอบไฟล์ผ่านฟังก์ชันที่เรียกว่า DWGCHECK ซึ่งฝังการตรวจสอบผลรวมที่เข้ารหัสและรหัสผลิตภัณฑ์ที่เรียกว่า WaterMark โดย Autodesk ลงในไฟล์ DWG ที่สร้างโดยโปรแกรม

**2006:** Autodesk แก้ไข AutoCAD 2007 เพื่อรวม "เทคโนโลยี TrustedDWG" เพื่อฝังสตริงข้อความ "Autodesk DWG ไฟล์นี้เป็น DWG ที่เชื่อถือได้ซึ่งบันทึกล่าสุดโดยแอปพลิเคชัน Autodesk หรือแอปพลิเคชันลิขสิทธิ์ของ Autodesk" ลงในไฟล์ DWG จุดประสงค์ของการดำเนินการนี้คือเพื่อช่วยให้ผู้ใช้ซอฟต์แวร์ Autodesk มั่นใจได้ว่าไฟล์เหล่านี้ถูกสร้างขึ้นโดยแอปพลิเคชัน Autodesk หรือ RealDWG ซึ่งจะช่วยลดความเสี่ยงของความไม่ลงรอยกันได้อย่างแน่นอน

## โครงสร้างไฟล์ ##

DWG เป็นหนึ่งในรูปแบบไฟล์ที่ใช้กันอย่างแพร่หลายโดยแอพพลิเคชั่นต่างๆ และมีโครงสร้างไฟล์ที่แข็งแกร่ง เนื่องจาก DWG เป็นรูปแบบไฟล์ไบนารี จึงไม่สามารถอ่านได้โดยมนุษย์เหมือนรูปแบบไฟล์ ASCII [DXF](/th/cad/dxf/) ธรรมดา ไฟล์ DWG มักจะมีข้อมูลเกี่ยวกับพิกัดรูปภาพและข้อมูลเมตาที่เกี่ยวข้อง [ข้อมูลจำเพาะ](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) ที่สมบูรณ์ของรูปแบบไฟล์ DWG พร้อมให้ดาวน์โหลดโดย OpenDesign โครงสร้างไฟล์ของรูปแบบไฟล์ DWG สรุปได้ดังนี้

**Header**: ส่วนหัวของไฟล์ประกอบด้วยตัวแปร DWG Header และข้อมูลเกี่ยวกับ Cyclic Redundancy Check (CRC) ซึ่งใช้สำหรับการตรวจจับข้อผิดพลาด แต่ละส่วนย่อยเป็นเวกเตอร์พิเศษที่ใช้บิตที่มีความยาวต่างกันเพื่อแสดงป้ายกำกับต่างๆ ตัวอย่างเช่น 6 บิตแรกของตัวแปร DWG Header หมายถึงสตริงเวอร์ชัน

**คำจำกัดความของคลาส:** ไฟล์ DWG อาจมีหลายคลาสขึ้นอยู่กับวัตถุประสงค์ของไฟล์ .dwg ที่เฉพาะเจาะจง ข้อมูลเช่นขนาดข้อมูลเมตาของคลาสของพื้นที่ข้อมูลคลาส หมายเลขคลาส และผลรวมตรวจสอบนอกเหนือจากข้อมูลอื่นๆ

**แม่แบบ**: เป็นทางเลือกสำหรับเวอร์ชัน R15 และ R15 ส่วนนี้จะอยู่ใต้ส่วนพื้นที่ว่างของวัตถุ

**ช่องว่างภายใน**: ข้อมูลเมตาจะต่อท้ายและต่อท้ายด้วยจำนวนไบต์ที่ระบุ ซึ่งทำให้ซอฟต์แวร์ AutoCAD เวอร์ชันเก่าสามารถส่งต่อไปยังรูปแบบไฟล์ DWG ใหม่ได้

**ข้อมูลรูปภาพ**: ข้อมูลเมตาสำหรับส่วนนี้ขึ้นอยู่กับประเภท .dwg ที่เฉพาะเจาะจง สำหรับผู้ใช้ R14 และ R15 ส่วนนี้เป็นทางเลือก

**ข้อมูลวัตถุ**: ข้อมูลวัตถุประกอบด้วยรายการที่สมบูรณ์ของเอนทิตีตาราง รายการพจนานุกรม ฯลฯ ที่สอดคล้องกับรายการวัตถุที่มีอยู่

**Object Map**: ตำแหน่งของแต่ละวัตถุในไฟล์ระบุไว้ในส่วนนี้ของไฟล์ ข้อมูลเมตาส่วนใหญ่ในส่วนนี้เป็นตัวจัดการไฟล์ที่มีบทบาทในการระบุตัวตนและการแสดงผลซ้ำของวัตถุ

**พื้นที่ว่างของวัตถุ**: ส่วนนี้เป็นทางเลือกสำหรับผู้ใช้ทุกคน

**Second Header**: ส่วนหัวของไฟล์ซ้ำกับส่วนท้ายของไฟล์ DWG

## อ้างอิง ##

* [ข้อกำหนดรูปแบบไฟล์ DWG](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [ข้อกำหนดไฟล์ DWG](https://www.scan2cad.com/dwg/file-spec/)
* [DWG - โดย Wikipedia](https://en.wikipedia.org/wiki/.dwg)
