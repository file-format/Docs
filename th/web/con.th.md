{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ CON - รูปแบบไฟล์แหล่งที่มาของแอปพลิเคชันแนวคิด",
  "description" :"เรียนรู้เกี่ยวกับไฟล์ CON และ API ที่สามารถสร้างและเปิดไฟล์ CON ได้",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## ไฟล์ CON คืออะไร??

ไฟล์ CON เป็นไฟล์ซอร์สโค้ดสำหรับแอปพลิเคชันที่พัฒนาขึ้นสำหรับ **Concept Application Server** ใช้สำหรับเขียนแอปพลิเคชันเพื่อแลกเปลี่ยนข้อมูลระหว่างเซิร์ฟเวอร์และผู้ใช้ ไฟล์ CON ที่โฮสต์บนเซิร์ฟเวอร์สามารถเข้าถึงได้ด้วยเว็บเบราว์เซอร์หากมีการติดตั้ง Concept Client ที่ปลายทางของผู้ใช้ Concept Application server เป็นเว็บเซิร์ฟเวอร์ที่มีภาษาการเขียนโปรแกรมขนาดเล็กที่อาจมีกลไกฐานข้อมูลชุดย่อย [SQL](/th/database/sql/) (TinDB)

ไฟล์ CON สามารถเปิด/รันด้วย RadGs Concept Application Server

## รูปแบบไฟล์ CON - ข้อมูลเพิ่มเติม

ไฟล์ CON ถูกโฮสต์บนเซิร์ฟเวอร์และเข้าถึงได้โดยใช้เว็บเบราว์เซอร์บนเครื่องของผู้ใช้ แนวคิด [URL](/th/web/url/) แตกต่างจาก URL HTTP ปกติและขึ้นต้นด้วย **concept://**

### ตัวอย่าง URL ไฟล์ CON

ไฟล์ CON ที่โฮสต์บน Concept Application Server สามารถเข้าถึงได้ผ่านเว็บเบราว์เซอร์โดยใช้ URL เช่น:

```
concept://domain.server.com/web_application/main.con.
```
## อ้างอิง

* [เซิร์ฟเวอร์แอปพลิเคชันแนวคิด](https://github.com/Devronium/ConceptApplicationServer)

