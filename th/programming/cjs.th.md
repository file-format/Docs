{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ไฟล์ CJS - ไฟล์รหัส CommonJS",
  "description":"ไฟล์ .cjs คืออะไร และจะเปิดได้อย่างไร",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-29"
}


## ไฟล์ CJS คืออะไร

ไฟล์ CommonJS (CJS) เป็นไฟล์ที่มีโค้ด JavaScript ที่เขียนด้วยไวยากรณ์ CommonJS CommonJS คือระบบโมดูลที่ออกแบบมาเพื่อทำงานในสภาพแวดล้อมนอกเหนือจากเว็บเบราว์เซอร์ส่วนหน้า และมักใช้ในสภาพแวดล้อม JavaScript ฝั่งเซิร์ฟเวอร์ เช่น Node.js

## รูปแบบไฟล์ CJS - ข้อมูลเพิ่มเติม

ไฟล์ CJS เขียนด้วยไวยากรณ์ CommonJS และสามารถแก้ไขได้ในโปรแกรมแก้ไขข้อความใด ๆ เช่น Microsoft Notepad หรือ Apple TextEdit โดยทั่วไปโมดูล CommonJS จะถูกจัดเก็บไว้ในไฟล์แยกกัน และมีวัตถุประสงค์เพื่อห่อหุ้มและทำให้โค้ดเป็นโมดูลเพื่อการจัดระเบียบและการบำรุงรักษาที่ดีขึ้น โมดูลเหล่านี้ใช้ฟังก์ชันที่จำเป็นในการนำเข้าการอ้างอิงและโมดูล module.exports หรือส่งออกวัตถุเพื่อแสดงค่าและฟังก์ชันที่ส่วนอื่น ๆ ของโค้ดสามารถใช้ได้

## ตัวอย่างโค้ด CJS

โมดูล CommonJS มีไวยากรณ์และโครงสร้างเฉพาะที่รวมคุณลักษณะต่างๆ เช่น ฟังก์ชันที่จำเป็นสำหรับการนำเข้าโมดูลอื่นๆ และ module.exports หรือส่งออกวัตถุสำหรับการส่งออกค่า ฟังก์ชัน หรือวัตถุจากโมดูล โมดูลเหล่านี้ใช้เพื่อห่อหุ้มและแยกส่วนของโค้ด ทำให้ง่ายต่อการจัดการและบำรุงรักษาโค้ดเบส JavaScript ขนาดใหญ่ นี่คือตัวอย่างพื้นฐานของโมดูล CommonJS:

```
// Module definition in a file named "myModule.js"
const someValue = 42;

function add(a, b) {
  return a + b;
}

module.exports = {
  someValue,
  add,
};

// Using the module in another file
const myModule = require('./myModule');
console.log(myModule.someValue); // 42
console.log(myModule.add(10, 20)); // 30
```

## อ้างอิง

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)