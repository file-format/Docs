{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ AGI - รูปแบบไฟล์อินเตอร์เฟส Asterisk Gateway",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ AGI พร้อมตัวอย่างและ API ที่สามารถสร้างและเปิดไฟล์ AGI ได้",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## ไฟล์ AGI คืออะไร??

ไฟล์ AGI เป็นไฟล์สคริปต์ที่ใช้โดยระบบโทรศัพท์โอเพ่นซอร์ส Asterisk ประกอบด้วยข้อมูลที่สามารถใช้เพื่อทำให้กระบวนการทำงานอัตโนมัติและแผนการหมุนหมายเลข Asterisk การใช้ไฟล์สคริปต์ AGI สามารถสร้างการเชื่อมต่อกับฐานข้อมูลเชิงสัมพันธ์ เช่น PostgreSQL หรือ MySQL นอกจากนี้ยังสามารถใช้สคริปต์ AGI เพื่อเข้าถึงทรัพยากรภายนอกอื่นๆ ได้อีกด้วย สคริปต์ AGI สามารถเปลี่ยนการควบคุมของไดอัลแพลนเป็นสคริปต์ AGI ภายนอก ทำให้ Asterisk สามารถทำงานที่ซับซ้อนได้

## รูปแบบไฟล์ AGI - ข้อมูลเพิ่มเติม

ไฟล์สคริปต์ AGI จะถูกบันทึกเป็นไฟล์ข้อความและสามารถเปิดได้ในโปรแกรมแก้ไขข้อความเพื่อทำการเปลี่ยนแปลง

### รูปแบบมาตรฐานของการสื่อสาร AGI

สคริปต์ AGI จะโหลดตัวแปรและค่าที่ส่งโดย Asterisk ลักษณะทั่วไปของตัวแปรเหล่านี้มีดังนี้

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

ตัวแปรเหล่านี้ตามด้วยบรรทัดว่างที่ส่งโดย Asterisk ซึ่งแสดงว่าสคริปต์ AGI สามารถควบคุมแผนการโทรได้แล้ว

### ภาษาโปรแกรมสำหรับไฟล์สคริปต์ AGI

โดยทั่วไปแล้ว สคริปต์ AGI สามารถเขียนด้วยภาษา Perl, [PHP](/th/programming/php/), [C](/th/programming/c/), Pascal หรือ Bourne Shell

## อ้างอิง

* [เครื่องหมายดอกจัน AGI](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

