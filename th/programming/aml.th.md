
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ AML - ไฟล์ภาษามาร์กอัปความช่วยเหลือของ Microsoft",
  "description":"เรียนรู้เกี่ยวกับไฟล์ AML และ API ที่สามารถสร้างและเปิดไฟล์ AML ได้",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML - ไฟล์ภาษามาร์กอัปความช่วยเหลือของ Microsoft

## ไฟล์ AML คืออะไร??

ไฟล์ AML (Assistance Markup Language) เป็นไฟล์ XML ที่สร้างด้วย Microsoft Assistance Markup Language (MAML) ได้รับการพัฒนาโดย Microsoft เพื่อให้ความช่วยเหลือออนไลน์สำหรับ Microsoft Windows OS ก่อนหน้านี้ ความช่วยเหลือของ Windows มีอยู่ในรูปแบบไฟล์ HTML [CHM](/th/web/chm/) ที่คอมไพล์แล้ว ไฟล์ AML มีเอกสารที่มีโครงสร้างที่ช่วยให้แอปพลิเคชันสร้างซอร์สโค้ดและสนับสนุนหน้าความช่วยเหลือ สิ่งนี้ช่วยให้คำจำกัดความของเอกสารและองค์ประกอบที่เป็นส่วนประกอบตามบริบท ไฟล์วิธีใช้ AML เผยแพร่ทางออนไลน์และสามารถกำหนดค่าเพื่อรับการอัปเดตจากการอัปเดตแพ็คเกจที่มีให้ทางออนไลน์

## โครงสร้างไฟล์ MAML

ไฟล์ AML ที่สร้างโดยใช้ MAML จะถูกบันทึกเป็นไฟล์ [XML](/th/web/xml/) ที่สามารถใช้แสดงแนวคิดที่ใช้งานอยู่ได้หลากหลาย นอกจากนี้ยังสามารถให้คำแนะนำช่วยเหลือ (ตัวช่วยสร้างเนื้อหาที่ใช้งานอยู่) ที่ทำให้ไฟล์วิธีใช้เป็นแบบโต้ตอบสำหรับผู้ใช้ด้วยตัวช่วยสร้างแบบทีละขั้นตอน

ไฟล์ AML ที่สร้างขึ้นโดยใช้ MAML เป็นไปตามโครงสร้างการเขียนที่สามารถแบ่งออกเป็นส่วนต่างๆ เช่น:

* แนวความคิด
* คำถามที่พบบ่อย
* อภิธานศัพท์
* ขั้นตอน
* อ้างอิง
* เนื้อหาที่นำมาใช้ใหม่
* งาน
* การแก้ไขปัญหาและ
* บทช่วยสอน

## จะสร้างไฟล์ MAML ได้อย่างไร?

ไฟล์ MAML สามารถสร้างได้โดยใช้วิธีใดวิธีหนึ่งต่อไปนี้:

* การใช้ Sandcastle - ใช้ชุดสคีมาและโปรแกรมปฏิบัติการเพื่อสร้างไฟล์วิธีใช้ อย่างไรก็ตาม เครื่องมือนี้ได้ถูกยกเลิกแล้ว
* การใช้ DocProject - ปลั๊กอิน Microsoft Visual Studio ที่สามารถดำเนินการได้จากภายใน Microsoft Visual Studio เพื่อสร้างเนื้อหาวิธีใช้

ไฟล์ MAML สามารถสร้างได้โดยใช้ Sandcastle ซึ่งเป็นชุดของ .XSL schema และโปรแกรมที่เรียกใช้งานได้ นอกจากนี้ยังอาจสร้างโดยใช้ DocProject ซึ่งเป็นโปรแกรมเสริมเครื่องมือช่วยเขียนของ Microsoft Visual Studio

## อ้างอิง

* [สร้างความช่วยเหลือแบบ XML โดยใช้ PlatyPS](https://learn.microsoft.com/en-us/powershell/scripting/dev-cross-plat/create-help-using-platyps?view=powershell-7.2)
* [ภาษามาร์กอัปของ Microsoft Assistance](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML - ไฟล์ภาษามาโครอาร์ค

## ไฟล์ ARC Macro AML คืออะไร??

ไฟล์ AML (ARC Macro Language) เป็นไฟล์สคริปต์ที่สร้างด้วยแอปพลิเคชัน ArcInfo Workstation GIS มันถูกเขียนด้วย ARC Macro Language ซึ่งเป็นภาษาอัลกอริธึมระดับสูงที่เป็นกรรมสิทธิ์สำหรับการสร้างแอปพลิเคชัน GIS ใน ArcInfo AML ได้รับการออกแบบโดย ESRI ในปี 1986 และตอบสนองวัตถุประสงค์ในการสร้างแอปพลิเคชันจากบรรทัดคำสั่งของระบบ ARCINFO GIS ในฐานะที่เป็นไฟล์สคริปต์ ไฟล์ AML สามารถมีคำสั่งสคริปต์เพื่อดำเนินการงานต่างๆ เช่น การสร้างส่วนประกอบส่วนติดต่อผู้ใช้และจัดการข้อมูลแผนที่

## รูปแบบไฟล์ AML - ข้อมูลเพิ่มเติม

AML เป็นไฟล์สคริปต์ บันทึกข้อมูลลงดิสก์เป็นไฟล์ข้อความธรรมดา เป็นไปตามไวยากรณ์ AML ซึ่งใช้ภาษาเชลล์ CPL ของระบบปฏิบัติการ PRIMOS ภาษา AML ถูกแทนที่ด้วยกรอบการประมวลผลทางภูมิศาสตร์ของ ESRI ซึ่งเป็นส่วนหนึ่งของชุดโปรแกรม ArcGIS และใช้ ArcObjects เพื่อให้การสนับสนุนการเขียนโปรแกรมผ่าน VBA หรือ Python

## อ้างอิง

* [ภาษามาโคร ARC](https://en.wikipedia.org/wiki/ARC_Macro_Language)
* [การใช้ AML กับเครื่องมือสคริปต์](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

