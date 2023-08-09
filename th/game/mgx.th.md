{
  "date" : "2021-09-08",
  "keywords" :[ "ไฟล์ mgx", "รูปแบบไฟล์ mgx", "ไฟล์ mgx คืออะไร", "ไฟล์", "ตัวอย่าง mgx", "นามสกุลไฟล์ mgx", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ Age of Empires 2 Expansion Replay MGX และ API ที่สามารถสร้างและเปิดไฟล์ MGX",
  "title" :"MGX - Age of Empires 2 Expansion Replay",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## ไฟล์ MGX คืออะไร??

ไฟล์ที่มีนามสกุล .mgx เป็นไฟล์ที่บันทึกสำหรับเกม Age of Empires II: The Conquerors ที่สามารถเล่นซ้ำได้ภายในโปรแกรม Age of Empires II มันมีการบันทึกที่สมบูรณ์ของแคมเปญที่เล่นโดยผู้ใช้ สามารถโหลดและเล่นได้ภายในโปรแกรม Age of Empires II เมื่อเล่นซ้ำ เกมจะแสดงเหตุการณ์และสถานการณ์ทั้งหมดที่ผู้ใช้วางแผนไว้สำหรับแคมเปญและเล่น

## รูปแบบไฟล์ MGX - ข้อมูลเพิ่มเติม

รูปแบบไฟล์ภายในของไฟล์ MGX ได้รับการปรับปรุงและพร้อมใช้งานเป็นข้อมูลที่ผ่านการตรวจสอบแล้วบางส่วนใน [Age of Empires 2: The Conquerors — ข้อมูลจำเพาะรูปแบบไฟล์ Savegame](https://github.com/stefan-kolb/aoc-mgx-format). ข้อมูลจำเพาะแสดงรายละเอียดในส่วนต่อไปนี้

### คำนิยามโครงสร้าง

คำจำกัดความโครงสร้างของรูปแบบไฟล์ GPX เชื่อว่าอิงตาม [การประกาศ BinData Ruby Gem](https://github.com/dmendel/bindata/wiki) ซึ่งมีวิธีอ่านและเขียนข้อมูลไบนารีที่มีโครงสร้าง ซึ่งช่วยให้โปรแกรมเมอร์ระบุรูปแบบของข้อมูลไบนารีที่ BinData อ่านและเขียนได้

### การส่งข้อความ MGX

การส่งข้อความ MGX ขึ้นอยู่กับข้อความสองประเภท

* GAMESTART - ระบุคำสั่งเริ่มเกมและยังไม่ได้ตรวจสอบความถูกต้องจนถึงปัจจุบัน
* แชท - อธิบายข้อความแชทในเกม ทั้งผู้เล่นและตัวเกม (ไกอา) สามารถส่งข้อความในเกมได้

### การกระทำในการเล่นเกม

มี [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) หลายรายการที่ได้รับการเรียกข้อมูลและมีรายละเอียด

## อ้างอิง

* [Age of Empires 2: The Conquerors — ข้อกำหนดรูปแบบไฟล์ Savegame](https://github.com/stefan-kolb/aoc-mgx-format)

