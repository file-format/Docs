{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ OBML - ไฟล์เว็บเพจที่บันทึกไว้ของ Opera Mini",
  "description" :"เรียนรู้เกี่ยวกับไฟล์ OBML และ API ที่สามารถสร้างและเปิดไฟล์ OBML ได้",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## ไฟล์ OBML คืออะไร??

ไฟล์ OBML (Opera Binary Markup Language) เป็นเวอร์ชันออฟไลน์ของหน้าเว็บที่บันทึกโดยเว็บเบราว์เซอร์มือถือ Opera Mini เป็นไฟล์ [HTML](/th/web/html/) เวอร์ชันกะทัดรัดที่มีองค์ประกอบในตัวทั้งหมด ซึ่งมีองค์ประกอบทั้งหมดของหน้าสำหรับแสดงบนอุปกรณ์เฉพาะขณะออฟไลน์ รูปแบบไฟล์ OBML ได้อัปเกรดเป็นหลายเวอร์ชันโดยใช้ OBML15 และ OBML16 เป็นจำนวนมาก ประเด็นสำคัญที่ควรคำนึงถึงคือ Opera Mini แต่ละเวอร์ชันเข้ากันได้กับรูปแบบ OBML เดียวเท่านั้น ดังนั้น การอัปเกรด Opera Mini จะทำให้สามารถอ่านหน้าที่บันทึกไว้ก่อนหน้านี้ได้ ไฟล์ OBML สามารถแปลงเป็น HTML และ [PDF](/th/pdf/)

## รูปแบบไฟล์ OBML

รูปแบบไฟล์ OBML ถูกบันทึกในรูปแบบไฟล์ที่เป็นกรรมสิทธิ์ของ Opera และข้อกำหนดรูปแบบไฟล์จะไม่เปิดเผยต่อสาธารณะ อย่างไรก็ตาม [รูปแบบ OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md) ได้รับการออกแบบวิศวกรรมย้อนกลับเพื่อถอดรหัสโครงสร้างดังต่อไปนี้

### ประเภทข้อมูล OBML

ตามผลลัพธ์ของวิศวกรรมย้อนกลับ OBML ใช้ประเภทดั้งเดิมต่อไปนี้:

* `byte` – จำนวนเต็มที่ไม่ได้ลงชื่อ (1 ไบต์)
* `short` – จำนวนเต็มที่มีลายเซ็น (2 ไบต์, big-endian)
* `medium` – จำนวนเต็มที่มีเครื่องหมาย (3 ไบต์, big-endian)
 * `blob` – { length: short, data: byte[length] }
* `char` – ไบต์ที่มีอักขระ ASCII
* `string` – blob ที่มีข้อความที่เข้ารหัส UTF-8

### ส่วนหัว OBML

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string,
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## อ้างอิง

* [รูปแบบ OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)

