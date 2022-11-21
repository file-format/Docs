{
  "date" : "2021-10-20",
  "keywords" :[ "ไฟล์ bns", "รูปแบบไฟล์ bns", "ไฟล์ bns คืออะไร", "ไฟล์", "ตัวอย่าง bns", "นามสกุลไฟล์ Portal Bonus Map Script","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ Ortal Bonus Map Script BNS และ API ที่สามารถสร้างและเปิดไฟล์ BNS",
  "title" :"BNS - ไฟล์สคริปต์แผนที่โบนัสพอร์ทัล",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## ไฟล์ BNS คืออะไร??

ไฟล์ที่มีนามสกุล .bns คือไฟล์สคริปต์เกมที่สร้างขึ้นด้วยเกมแก้ปริศนา Portal Map ที่พัฒนาโดย Valve ประกอบด้วยสคริปต์ข้อความสำหรับกำหนดข้อมูลเกี่ยวกับแผนที่พอร์ทัลซึ่งจัดเก็บเป็นไฟล์ .bsp ไฟล์ BNS ใช้เป็นข้อมูลอ้างอิงถึงไฟล์แผนที่จริงนี้ และมีรายการความท้าทายที่ต้องดำเนินการให้เสร็จสิ้น นอกจากนี้ยังมีชื่อแผนที่ ความคิดเห็นเกี่ยวกับแผนที่ และการอ้างอิงไฟล์ภาพขนาดย่อ ไฟล์ BNS สามารถเปิดได้ในโปรแกรมแก้ไขข้อความใดๆ เช่น Notepad++, textEdit และ Notepad

## รูปแบบไฟล์ BNS

ไฟล์ BNS จะถูกบันทึกเป็นไฟล์ข้อความธรรมดาที่มนุษย์สามารถอ่านได้ สามารถเปิดในโปรแกรมแก้ไขข้อความและแก้ไขได้เช่นกัน อย่างไรก็ตาม ควรแก้ไขอย่างระมัดระวังเพื่อหลีกเลี่ยงข้อผิดพลาดในสคริปต์

## ตัวอย่างรูปแบบไฟล์ BNS

ไฟล์ BNS อาจมีลักษณะดังต่อไปนี้เมื่อเปิดในโปรแกรมแก้ไขข้อความ เช่น Notepad++

```
"#Bonus_Map_Challenges"
{
	"map"		"testchmb_a_08"
	"chapter"	"chapter5.cfg"	[$X360]
	"image"		"bonusmaps/testchmb_a_08_challenges"
	"comment"	"#Bonus_Map_ChallengesComment"
	"lock"		"0"

	"challenges"
	{
		"#Bonus_Map_ChallengePortals"
		{
			"comment"	"#Bonus_Map_LeastPortalsComment"

			"bronze"	"9"
			"silver"	"5"
			"gold"		"4"
		}
		"#Bonus_Map_ChallengeSteps"
		{
			"comment"	"#Bonus_Map_LeastStepsComment"

			"bronze"	"30"
			"silver"	"20"
			"gold"		"10"
		}
		"#Bonus_Map_ChallengeTime"
		{
			"comment"	"#Bonus_Map_LeastTimeComment"

			"bronze"	"40"
			"silver"	"30"
			"gold"		"19"
		}
	}
}
```

## ส่วนต่างๆ ของไฟล์ BNS

ในตัวอย่างข้างต้น

* `#Bonus_Map_Challenges` - แสดงชื่อแผนที่
* `map` - แสดงชื่อแผนที่ที่จะใส่ในโฟลเดอร์แผนที่ของเกม
* `บทที่' - แสดงถึงบทที่เป็นของแผนที่ ไฟล์บททั้งหมดอยู่ในไฟล์ VPK โดยเพิ่มชื่อแผนที่ในรูปแบบ `map your_map_name`
* `Image` - ประกอบด้วยภาพขนาดย่อของแผนที่และจัดเก็บไว้ที่เส้นทางรูท steam\steamapps\common\portal\portal\materials\VGUI
* `ความคิดเห็น` - ข้อความอธิบายเกี่ยวกับแผนที่ที่สร้างขึ้น

## อ้างอิง

* [สคริปต์ท้าทายพอร์ทัล](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

