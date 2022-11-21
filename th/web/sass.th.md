---
date: 2019-10-11
keywords: sass, .sass, รูปแบบไฟล์ sass, วิธีเปิดไฟล์ sass, สไตล์ชีตที่ยอดเยี่ยมทางวากยสัมพันธ์, ตัวประมวลผลล่วงหน้า css, sass,
ผู้เขียน:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: รูปแบบไฟล์ Sass,
linktitle: Sass
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ Sass และ API ที่สามารถสร้างและเปิดไฟล์ Sass"
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## ไฟล์ SASS คืออะไร?? ##

Sass (สไตล์ชีตที่ยอดเยี่ยมทางวากยสัมพันธ์) เป็นภาษาสคริปต์ตัวประมวลผลล่วงหน้า มันถูกคอมไพล์เป็น [CSS](/th/web/css/) และจัดเก็บด้วยนามสกุล .sass Sass ประกอบด้วยสองไวยากรณ์ ต้นฉบับใช้การเยื้องที่ใช้ส่วนขยาย .sass และ SCSS รุ่นใหม่ที่มีรูปแบบบล็อกเช่น CSS ที่ใช้ส่วนขยาย .scss

## ทำไมต้องใช้ Sass ##

Sass มีประโยชน์อย่างมากในการรักษาสไตล์ เนื่องจากมีคุณสมบัติมากมาย เช่น การแนะนำตัวแปร การซ้อน มิกซ์อิน การนำเข้า และการสืบทอดตัวเลือกที่ทำให้การทำงานกับสไตล์เป็นเรื่องสนุก

## วิธีใช้ไฟล์ SASS ##

ไฟล์ SASS ไม่ได้รวมอยู่ในเอกสาร [HTML](/th/web/html/) โดยตรง แต่จะถูกแปลงเป็นไฟล์ CSS ที่รวมอยู่ในไฟล์ HTML คุณสามารถติดตั้ง Sass ในระบบของคุณได้โดยทำตามคำแนะนำที่ให้ไว้ใน [เว็บไซต์ Sass อย่างเป็นทางการ] (https://sass-lang.com/install)

Sass อาจถูกแปลงเป็น CSS โดยการแปลงไฟล์ SASS ที่บันทึกไว้แล้ว หรือโดยการเฝ้าดูการเปลี่ยนแปลงและแปลงเมื่อบันทึกไฟล์ คำสั่งสำหรับทั้งสองได้รับด้านล่าง

### แปลงครั้งเดียว ###

พารามิเตอร์แรกของคำสั่งคือไฟล์ SASS ต้นทาง และพารามิเตอร์ที่สองคือไฟล์ CSS เอาต์พุต

```cmd
sass main.sass main.css
```

### เฝ้าดูการเปลี่ยนแปลง ###

คำสั่งดังกล่าวสามารถรันได้ด้วยแฟล็ก *watch* เพิ่มเติมที่ทำให้คำสั่งทำงานต่อไป และทันทีที่บันทึกไฟล์ Sass เอาต์พุต CSS จะถูกสร้างขึ้น

```cmd
sass --watch main.sass main.css
```

## ไวยากรณ์ Sass ##

Sass รองรับตัวแปร, การซ้อน, มิกซ์อิน, อิมพอร์ต, การสืบทอดตัวเลือก ฯลฯ ด้านล่างนี้เป็นตัวอย่างของคุณสมบัติเหล่านี้

### ตัวแปร ###

สามารถใช้ตัวแปรเพื่อตั้งค่าข้อมูลที่ใช้ซ้ำได้ เช่น สีหลักหรือช่องว่างภายในสำหรับปุ่ม สิ่งนี้สามารถพิสูจน์ได้ว่ามีประโยชน์หากในอนาคตคุณต้องการเปลี่ยนแปลงข้อมูลนั้น คุณเพียงแค่เปลี่ยนที่เดียวและจะอัปเดตทุกที่

**สัส**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**สร้าง CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### การทำรัง ###

ตัวเลือก CSS สามารถซ้อนกันคล้ายกับลำดับชั้นของ HTML ในตัวอย่างต่อไปนี้ สแปนซ้อนอยู่ภายในบล็อก h1

**สัส**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**สร้าง CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### มิกซ์ ###

มิกซ์อินใช้เพื่อจัดกลุ่มคุณสมบัติที่คล้ายกันเข้าด้วยกันซึ่งใช้ในหลายแห่ง มิกซ์อินยังรองรับพารามิเตอร์อีกด้วย

**สัส**

**ประกาศผสม**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**ใช้มิกซ์อิน**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**สร้าง CSS**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### ขยาย ###

การขยาย/การสืบทอดสามารถพิสูจน์ได้ว่ามีประโยชน์ในกรณีที่จำเป็นต้องแชร์คุณสมบัติของตัวเลือกหนึ่งกับตัวเลือกอื่น ในตัวอย่างด้านล่าง ตัวเลือก *.error-notice* ใช้คุณสมบัติทั้งหมดของตัวเลือก *.error-text* และเพิ่มคุณสมบัติเส้นขอบและการเติม

**สัส**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
```

**สร้าง CSS**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### นำเข้า ###

การนำเข้าอาจมีประโยชน์หากคุณจัดโครงสร้างสไตล์ของคุณเป็นไฟล์ต่างๆ ตามฟังก์ชันการทำงานหรือโครงสร้างอื่นๆ ที่คุณปฏิบัติตาม คุณสามารถนำเข้าไฟล์ทั้งหมดเหล่านี้ในไฟล์ SASS หลักที่แปลงเป็น CSS ในภายหลัง ขณะนำเข้า คุณไม่จำเป็นต้องระบุนามสกุลไฟล์ในคำสั่งนำเข้า Sass รวบรวมไฟล์ SASS ทั้งหมดโดยตรง หากต้องการหลีกเลี่ยงการคอมไพล์ไฟล์อิมพอร์ตโดยตรง คุณสามารถทำให้ไฟล์เหล่านี้บางส่วนได้โดยเพิ่มเครื่องหมายขีดล่าง (_) ที่จุดเริ่มต้นของชื่อไฟล์ นำเข้าบางส่วนคล้ายกับไฟล์ Sass ทั่วไป

**สัส**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

CSS เอาต์พุตจะมีสไตล์จากไฟล์ที่นำเข้าทั้งหมด

## อ้างอิง ##

- [Sass - วิกิพีเดีย](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

