---
date: 2019-10-11
keywords: css, .css, รูปแบบไฟล์ css, วิธีเปิดไฟล์ css, สไตล์ชีตแบบเรียงซ้อน,
ผู้เขียน:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: รูปแบบไฟล์ CSS,
linktitle: CSS
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ CSS และ API ที่สามารถสร้างและเปิดไฟล์ CSS"
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## ไฟล์ CSS คืออะไร? ##

CSS (Cascading Style Sheets) เป็นไฟล์ที่อธิบายวิธีแสดงองค์ประกอบ HTML บนหน้าจอ กระดาษ ฯลฯ ด้วย HTML คุณสามารถกำหนดสไตล์ที่ฝังไว้หรือสไตล์ที่สามารถกำหนดได้ในสไตล์ชีตภายนอก สำหรับการฝังสไตล์ \ <style>\</style> มีการใช้แท็ก สไตล์ชีตภายนอกถูกจัดเก็บไว้ในไฟล์ที่มีนามสกุล .css ด้วย CSS ภายนอก คุณสามารถรวมไว้ในหน้า HTML หลายหน้าเพื่ออัปเดตสไตล์ของหน้าเหล่านั้น แม้แต่ไฟล์ CSS ไฟล์เดียวก็สามารถใช้จัดรูปแบบเว็บไซต์ที่สมบูรณ์ได้

## ประวัติย่อ ##

CSS1 เปิดตัวในปี 1996 โดยมี Bert Bos เป็นผู้เขียนร่วม คณะทำงาน CSS เริ่มทำงานในประเด็นที่ไม่ได้กล่าวถึงใน CSS1 ส่งผลให้มีการสร้าง CSS2 ในเดือนพฤศจิกายน พ.ศ. 2540 ซึ่งเผยแพร่เป็นคำแนะนำของ W3C เมื่อวันที่ 12 พฤษภาคม พ.ศ. 2541 เวอร์ชันนี้เพิ่มการสนับสนุนสำหรับอุปกรณ์เฉพาะสื่อ เช่น เครื่องพิมพ์ แบบอักษรที่ดาวน์โหลดได้ ตาราง และการวางตำแหน่งองค์ประกอบ ในเดือนมิถุนายน พ.ศ. 2542 CSS3 ได้กลายเป็นคำแนะนำของ W3C สิ่งนี้แบ่งเอกสารออกเป็นโมดูลโดยแต่ละโมดูลมีคุณลักษณะส่วนขยายที่กำหนดไว้ใน CSS2

## วิธีใช้ไฟล์ CSS ##

หากต้องการใช้ไฟล์ CSS ให้ใส่ไว้ในส่วนหัวของเอกสาร HTML คุณใช้แท็กลิงก์เพื่อรวมไฟล์ที่แสดงด้านล่าง

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

แอตทริบิวต์ *href* ของแท็กลิงก์มีเส้นทางไปยังไฟล์ CSS เมื่อทำเช่นนี้ สไตล์ที่ใช้ได้ที่มีอยู่ในไฟล์ CSS ที่รวมไว้จะถูกนำไปใช้กับเอกสาร HTML

## ไวยากรณ์ CSS ##

กฎ CSS ประกอบด้วยสององค์ประกอบ ตัวเลือก และการประกาศ ตัวเลือกชี้ไปที่องค์ประกอบในเอกสาร HTML สามารถเป็นได้ทั้งแท็กองค์ประกอบ ชื่อคลาส ชื่อรหัส หลายแท็กที่แสดงลำดับชั้น ฯลฯ การประกาศประกอบด้วยคำนิยามสไตล์ที่ประกอบด้วยคุณสมบัติและค่า คุณสมบัติระบุคุณสมบัติขององค์ประกอบที่คุณต้องการเปลี่ยนแปลงและค่าจะกำหนดค่าใหม่ กฎ CSS แต่ละข้อสามารถมีการประกาศได้หลายรายการ ต่อไปนี้เป็นตัวอย่างของกฎ CSS

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

ในตัวอย่างข้างต้น เรามี **h1** เป็นตัวเลือกที่เลือกแท็ก h1 ทั้งหมดในเอกสาร HTML กฎมีการประกาศสองรายการ หนึ่งรายการสำหรับน้ำหนักแบบอักษร และอีกรายการหนึ่งสำหรับสี *font-weight* และ *color* เป็นคุณสมบัติ และ *700* และ *forestgreen* เป็นค่าตามลำดับ

## ตัวอย่างการใช้ CSS ##

ต่อไปนี้แสดงตัวอย่างเอกสาร HTML และสไตล์ชีตที่ใช้จัดรูปแบบ ภาพเปรียบเทียบจะถูกเพิ่มเพื่อเปรียบเทียบเอกสาร HTML ที่มีสไตล์และธรรมดา

### เอกสาร HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### สไตล์ชีต CSS ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### การเปรียบเทียบผลลัพธ์ ###

ด้านซ้ายของรูปภาพแสดงเอกสาร HTML โดยไม่ใช้สไตล์ และด้านขวาแสดงเอกสาร HTML โดยไม่ใช้สไตล์

{{< figure src="../CssExample.jpg" alt="ภาพตัวอย่าง" >}}

## อ้างอิง ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

