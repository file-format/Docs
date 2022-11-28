{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ vsdm", "รูปแบบไฟล์ vsdm", "ไฟล์ vsdm คืออะไร", "ไฟล์", "ตัวอย่าง vsdm", "นามสกุลไฟล์ vsdm", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM - รูปแบบไฟล์ Microsoft Visio Drawing",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ VSDM และ API ที่สามารถสร้างและเปิดไฟล์ VSDM",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ VSDM คืออะไร??

ไฟล์ที่มีนามสกุล .vsdm เป็นไฟล์รูปวาดที่สร้างด้วยแอปพลิเคชัน Microsoft Visio ที่รองรับมาโคร ไฟล์ VSDM เป็นภาพวาด OPC/XML ที่คล้ายกับ VSDX แต่ยังให้ความสามารถในการเรียกใช้มาโครเมื่อเปิดไฟล์ แมโครคือการกระทำ/ขั้นตอนที่ผู้ใช้กำหนดซึ่งพัฒนาขึ้นใน Visual Basic for Applications (VBA) และสามารถใช้เพื่อทำงานซ้ำๆ รูปแบบไฟล์ VSDM ถูกนำมาใช้พร้อมกับการเปิดตัว Microsoft Visio 2013 ไฟล์ Visio ถูกใช้เพื่อสร้างภาพวาดที่มีวัตถุภาพ แผนภูมิลำดับงาน ไดอะแกรม UML โฟลว์ข้อมูล แผนผังองค์กร ไดอะแกรมซอฟต์แวร์ โครงร่างเครือข่าย แบบจำลองฐานข้อมูล การแมปวัตถุ และอื่นๆ ข้อมูลที่คล้ายกัน ไฟล์ที่สร้างโดยใช้ Visio ยังสามารถส่งออกเป็นรูปแบบไฟล์ต่างๆ เช่น [PNG](/th/image/png/), [BMP](/th/image/bmp/), [PDF](/th/pdf/) และอื่นๆ

## รูปแบบไฟล์ VSDM

ไฟล์ VSDM อิงตาม Open Packaging Conventions และ XML และนักพัฒนาสามารถได้รับประโยชน์จากรูปแบบนี้โดยการเรียนรู้วิธีการทำงานกับไฟล์เหล่านี้ทางโปรแกรม รูปแบบสืบทอดโครงสร้าง XML เดียวกันหลายส่วนจากรูปแบบไฟล์ Visio XML Drawing (.vdx) ความสามารถในการทำงานร่วมกันกับไฟล์ Visio นั้นเพิ่มขึ้นอย่างมาก เนื่องจากซอฟต์แวร์ของบริษัทอื่นสามารถจัดการไฟล์ Visio ในระดับรูปแบบไฟล์ได้

ไฟล์ Visio แต่ละไฟล์เรียกว่าแพ็คเกจที่เก็บไฟล์หรือส่วนอื่นๆ ส่วนของแพ็คเกจสามารถเป็นไฟล์ XML รูปภาพ หรือแม้แต่โซลูชัน VBA ส่วนต่างๆ ภายในแพ็คเกจสามารถแบ่งออกเป็นส่วน "เอกสาร" และ "ความสัมพันธ์"

### เอกสาร ###

ส่วนของเอกสารประกอบด้วยเนื้อหาจริงและข้อมูลเมตาของไฟล์ Visio เช่น ชื่อของไฟล์ หน้าแรก และรูปร่างทั้งหมดที่มีอยู่ และแม้แต่การเชื่อมต่อข้อมูลสำหรับรูปร่าง ไฟล์รูปภาพและข้อความภายในแพ็คเกจถือเป็นส่วนของเอกสาร

### ความสัมพันธ์ ###

ส่วนต่างๆ ของความสัมพันธ์ของไฟล์ Visio จะถูกจัดเก็บไว้ในโฟลเดอร์ "\_rels" และอธิบายว่าส่วนต่างๆ ภายในแพ็กเกจมีความเกี่ยวข้องกันอย่างไร นอกจากนี้ยังให้โครงสร้างของไฟล์ เอกสาร XML แบบสแตนด์อโลนใช้ความสัมพันธ์หลัก/รองขององค์ประกอบเพื่อกำหนดความสัมพันธ์ของเอนทิตีซึ่งกันและกัน รูปแบบไฟล์ Visio 2013 ที่ถูกต้องประกอบด้วยชุดของส่วนที่ถูกต้อง และแพคเกจประกอบด้วยความสัมพันธ์ระหว่างส่วนต่างๆ

ส่วนความสัมพันธ์คือเอกสาร XML ที่อธิบายความสัมพันธ์ระหว่างส่วนต่างๆ ของเอกสารภายในแพ็คเกจ กำหนดความสัมพันธ์ระหว่างสองรายการ: แหล่งที่มาที่ระบุ (กำหนดโดยชื่อและตำแหน่งของไฟล์ความสัมพันธ์) และส่วนเอกสารเป้าหมายที่ระบุ ตัวอย่างเช่น ส่วนต่างๆ ของความสัมพันธ์ถูกใช้เพื่ออธิบายว่าต้นแบบรูปร่างใดเชื่อมโยงกับไฟล์ เพจเกี่ยวข้องกับไฟล์และเกี่ยวข้องกันอย่างไร หรือรูปภาพและวัตถุเกี่ยวข้องกับเพจใดเพจหนึ่งอย่างไร

## อ้างอิง ##

* [ความรู้เบื้องต้นเกี่ยวกับรูปแบบไฟล์ Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)
