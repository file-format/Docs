---
date: 2019-10-11
keywords: js, .js, รูปแบบไฟล์ js, วิธีเปิดไฟล์ js, ไฟล์จาวาสคริปต์,
ผู้เขียน:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: รูปแบบไฟล์ JS,
linktitle: JS
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ JS และ API ที่สามารถสร้างและเปิดไฟล์ JS"
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## ไฟล์ JS คืออะไร?? ##

JS (JavaScript) คือไฟล์ที่มีโค้ด JavaScript สำหรับดำเนินการบนหน้าเว็บ ไฟล์ JavaScript ถูกจัดเก็บด้วยนามสกุล .js ภายในเอกสาร [HTML](/th/web/html/) คุณสามารถฝังโค้ด JavaScript โดยใช้ปุ่ม \ <script>\</script> แท็กหรือรวมไฟล์ JS คล้ายกับไฟล์ [CSS](/th/web/css/) ไฟล์ JS สามารถรวมไว้ในเอกสาร HTML หลายฉบับเพื่อให้โค้ดกลับมาใช้ใหม่ได้ JavaScript สามารถใช้เพื่อจัดการ HTML DOM

## ประวัติย่อ ##

JavaScript จัดส่งครั้งแรกโดยเป็นส่วนหนึ่งของ Navigator Browser ในเดือนกันยายน พ.ศ. 2538 โดยใช้ชื่อ LiveScript โดย Netscape มันถูกเปลี่ยนชื่อเป็น JavaScript ในสามเดือนต่อมา ในปี 1996 Microsoft ได้ทำการวิศวกรรมย้อนกลับของ Navigator เพื่อสร้าง JScript JScript เปิดตัวพร้อมกับ Internet Explorer และแตกต่างจาก JavaScript อย่างมาก

Netscape ส่ง JavaScript ไปยัง ECMA International ซึ่งนำไปสู่การเปิดตัวข้อกำหนด ECMAScript ตัวแรกอย่างเป็นทางการในปี 1997 ECMAScript 2 เปิดตัวในปี 1998 ECMAScript 3 ในปี 1999 และการทำงานบน ECMAScript 4 เริ่มในปี 2000 แต่ยังไม่บรรลุผล

Jesse James Garrett ในปี 2548 ได้ออกเอกสารไวท์เปเปอร์ซึ่งเขาได้บัญญัติคำว่า *Ajax* สิ่งนี้ใช้ JavaScript เป็นแกนหลักในการสร้างเว็บแอปพลิเคชันที่โหลดข้อมูลในพื้นหลังและหลีกเลี่ยงการโหลดซ้ำทั้งหน้า ส่งผลให้มีการสร้างไลบรารีเช่น JQuery, Prototype, Dojo เป็นต้น

Google เปิดตัวเบราว์เซอร์ Chrome พร้อมเอ็นจิ้น V8 JavaScript ในปี 2008 ในช่วงต้นปี 2009 มีการทำข้อตกลงเพื่อรวมงานที่เกี่ยวข้องทั้งหมดและขับเคลื่อน JavaScript ไปข้างหน้า ส่งผลให้มีการเปิดตัวมาตรฐาน ECMAScript 5 ในเดือนธันวาคม 2552

## วิธีใช้ไฟล์ JS ##

หากต้องการใช้ไฟล์ JS ให้รวมไว้ในเอกสาร HTML คุณใช้แท็กลิงก์เพื่อรวมไฟล์ที่แสดงด้านล่าง

```html
<script src="site.js"></script>
```

แอตทริบิวต์ *src* ของแท็ก *script* มีพาธไปยังไฟล์ JS เมื่อทำเช่นนี้ ฟังก์ชัน JS จะถูกเพิ่มลงในเอกสาร HTML

## ไวยากรณ์ JS ##

ไฟล์ JavaScript สามารถมีตัวแปร ตัวดำเนินการ ฟังก์ชัน เงื่อนไข ลูป อาร์เรย์ ออบเจกต์ ฯลฯ ด้านล่างเป็นภาพรวมโดยย่อของไวยากรณ์ของ JavaScript

- แต่ละคำสั่งลงท้ายด้วยเครื่องหมายอัฒภาค (;)
- ใช้คีย์เวิร์ด *var* เพื่อประกาศตัวแปร
- รองรับตัวดำเนินการทางคณิตศาสตร์ ( + - * / ) เพื่อคำนวณค่า
- ความคิดเห็นบรรทัดเดียวถูกเพิ่มด้วย // และความคิดเห็นหลายบรรทัดล้อมรอบด้วย /* และ */
- ตัวระบุทั้งหมดคำนึงถึงขนาดตัวพิมพ์ เช่น *modelNo* และ *modelno* เป็นสองตัวแปรที่แตกต่างกัน
- ฟังก์ชันถูกกำหนดโดยใช้คีย์เวิร์ด *function*
- อาร์เรย์สามารถกำหนดได้โดยใช้วงเล็บเหลี่ยม []
- JS รองรับตัวดำเนินการเปรียบเทียบเช่น ==, != , >=, !== เป็นต้น
- คลาสสามารถกำหนดได้โดยใช้คีย์เวิร์ด *คลาส*

## ตัวอย่างการใช้งาน JS ##

ต่อไปนี้เป็นไฟล์ JavaScript ตัวอย่างการใช้งานอย่างง่าย

### เอกสาร HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### รหัส JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## อ้างอิง ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

