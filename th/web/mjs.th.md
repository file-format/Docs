{
  "date" : "2021-07-20",
  "keywords" :["MJS", "ไฟล์", "นามสกุล", "รูปแบบไฟล์", "นามสกุลไฟล์", "ไฟล์โมดูล Node.js ES"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - ไฟล์ Javascript โมดูล Node.js ES",
  "description" :"เรียนรู้เกี่ยวกับไฟล์ MJS และ API ที่สามารถสร้างและเปิดไฟล์ MJS ได้",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## ไฟล์ MJS คืออะไร??

ไฟล์ที่มีนามสกุล .mjs คือไฟล์ซอร์สโค้ด JavaScript ที่ใช้เป็นโมดูล ECMA (โมดูล ECMAScript) ในแอปพลิเคชัน Node.js ระบบโมดูล natvie ของ Node.js คือ CommonJS ที่ใช้ในการแยกโค้ดในไฟล์ต่างๆ เพื่อให้โค้ด [JS](/th/web/js/) เป็นระเบียบ MJS เป็นวิธีเดียวที่ Node.js ใช้เพื่อระบุว่าโมดูลนั้นเป็น CommonJS หรือ ES6 โมดูล ECMAScript เป็นรูปแบบมาตรฐานสำหรับการบรรจุรหัส JavaScript เพื่อนำมาใช้ซ้ำ ไฟล์ MJS สามารถเปิดได้ในโปรแกรมแก้ไขข้อความ เช่น Atom, Vim, Apple xCode, Microsoft Visual Studio และ Notepad

## รูปแบบไฟล์ MJS - ข้อมูลเพิ่มเติม

ไฟล์ MJS ถูกบันทึกลงดิสก์เป็นรูปแบบข้อความธรรมดาในไวยากรณ์ JavaScript สิ่งเหล่านี้สามารถเปิดได้ในโปรแกรมแก้ไขข้อความใด ๆ และมนุษย์สามารถอ่านได้ ตั้งแต่ปี 2018 เบราว์เซอร์หลักเกือบทั้งหมดรองรับโมดูล ES

## ความแตกต่างระหว่างโมดูล ES และ CommonJS

อะไรทำให้ไฟล์ MJS แตกต่างจากไฟล์ JS ธรรมดา สรุปความแตกต่างระหว่าง ES Modules และ CommonJS ได้ดังนี้

* ไม่ต้องการ ส่งออก หรือ module.exports
* ไม่มี \__ชื่อไฟล์ หรือ \__dirname
* ไม่มีการโหลดโมดูล JSON
* ไม่มีการโหลดโมดูลเนทีฟ
* ไม่ต้องการแก้ไข
* ไม่มี NODE_PATH
* ไม่จำเป็นต้องใช้ส่วนขยาย
* ไม่จำเป็นต้องใช้แคช

## อ้างอิง

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [ความแตกต่างระหว่าง JS และ MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

