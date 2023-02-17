{
  "date" : "2021-06-14",
  "keywords" :[ "LOG", "นามสกุล", "ไฟล์บันทึก", "รูปแบบไฟล์บันทึก", "ประเภทไฟล์ฐานข้อมูล", "รูปแบบไฟล์ฐานข้อมูล", "ไฟล์บันทึกคืออะไร" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ LOG และ API ที่สามารถสร้างและเปิดไฟล์ LOG",
  "title" :"LOG - รูปแบบไฟล์บันทึก",
  "linktitle" : "LOG",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## ไฟล์ LOG คืออะไร?
ไฟล์ที่มีนามสกุล .log มีรายการข้อความล้วนที่มีการประทับเวลา โดยปกติแล้ว รายละเอียดกิจกรรมบางอย่างจะถูกบันทึกโดยซอฟต์แวร์หรือระบบปฏิบัติการเพื่อช่วยให้นักพัฒนาหรือผู้ใช้สามารถติดตามสิ่งที่เกิดขึ้นในช่วงเวลาหนึ่งๆ ผู้ใช้สามารถแก้ไขไฟล์เหล่านี้ได้อย่างง่ายดายโดยใช้โปรแกรมแก้ไขข้อความใดๆ โดยปกติแล้ว รายงานข้อผิดพลาดหรือกิจกรรมการเข้าสู่ระบบจะถูกบันทึกโดยระบบปฏิบัติการ แต่ซอฟต์แวร์หรือเว็บเซิร์ฟเวอร์อื่นๆ ยังสร้างไฟล์บันทึกเพื่อติดตามผู้เยี่ยมชมและตรวจสอบการใช้แบนด์วิธ

## รูปแบบไฟล์บันทึก
รูปแบบไฟล์ LOG จะบันทึกเหตุการณ์ทั่วไปที่เกิดขึ้นในระบบปฏิบัติการ ข้อความระหว่างผู้ใช้ที่แตกต่างกันของซอฟต์แวร์สื่อสาร หรือซอฟต์แวร์อื่นที่รัน เราสามารถพูดง่ายๆ ว่าข้อความบางข้อความ ณ เวลาที่แน่นอนถูกบันทึกไว้ในไฟล์ LOG คำศัพท์ที่ใช้กันทั่วไปสำหรับการบันทึกคือ:
### บันทึกเหตุการณ์
บันทึกเหตุการณ์ที่เกิดขึ้นในการดำเนินการของระบบเพื่อติดตามและทำความเข้าใจกิจกรรมของระบบและเพื่อวินิจฉัยปัญหา มีความสำคัญในการระบุกิจกรรมของระบบที่ซับซ้อน โดยทั่วไปในกรณีของแอปพลิเคชันที่มีการโต้ตอบกับผู้ใช้น้อยมาก
### บันทึกการทำธุรกรรม
ระบบฐานข้อมูลเกือบทั้งหมดจะเก็บรักษาบันทึกการทำธุรกรรม ซึ่งโดยปกติแล้วไม่ได้มีไว้เพื่อเป็นร่องรอยการตรวจสอบสำหรับการวิเคราะห์ในภายหลัง และมนุษย์ไม่สามารถอ่านได้ บันทึกเหล่านี้เก็บเฉพาะบันทึกการเปลี่ยนแปลงข้อมูลที่มีอยู่เพื่อให้ฐานข้อมูลสามารถกู้คืนจากการขัดข้องหรือข้อผิดพลาดของข้อมูลอื่น ๆ และเก็บข้อมูลในสถานะที่สอดคล้องกัน ดังนั้น ระบบฐานข้อมูลมักจะมีทั้งบันทึกเหตุการณ์ทั่วไปและบันทึกธุรกรรม
### บันทึกข้อความ
การสื่อสารด้วยข้อความที่บันทึกไว้โดย Internet Relay Chat (IRC), โปรแกรมส่งข้อความโต้ตอบแบบทันที (IM), ไคลเอ็นต์การแชร์ไฟล์แบบ peer-to-peer ด้วยฟังก์ชันแชท และเกมแบบผู้เล่นหลายคน (โดยเฉพาะ MMORPG) เรียกว่า บันทึกข้อความ บันทึกเหล่านี้โดยทั่วไปจะบันทึกเป็นไฟล์ข้อความธรรมดา แต่ไคลเอนต์ IM และ VoIP (เช่น Skype) อาจบันทึกเป็นไฟล์ HTML เพื่อให้อ่านง่ายหรือเปิดใช้งานการเข้ารหัส
### บันทึกเซิร์ฟเวอร์
บันทึกของเซิร์ฟเวอร์เป็นไฟล์บันทึกที่มีรายการกิจกรรมที่ดำเนินการและสร้างหรือดูแลโดยอัตโนมัติโดยเซิร์ฟเวอร์เอง โดยปกติแล้วไฟล์เหล่านี้จะไม่สามารถเข้าถึงได้โดยผู้ใช้อินเทอร์เน็ตทั่วไป เฉพาะกับเว็บมาสเตอร์หรือผู้ดูแลระบบอื่นๆ ของบริการอินเทอร์เน็ตเท่านั้น



## อ้างอิง ##

* [ไฟล์บันทึก - Wikipedia](https://en.wikipedia.org/wiki/Log_file)
