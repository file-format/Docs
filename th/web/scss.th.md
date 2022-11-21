---
date: 2019-10-11
keywords: scss, .scss, รูปแบบไฟล์ scss, วิธีเปิดไฟล์ scss, สไตล์ชีตที่ยอดเยี่ยมทางวากยสัมพันธ์, ตัวประมวลผลล่วงหน้า css, sass,
ผู้เขียน:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: รูปแบบไฟล์ SCSS - Sass Cascading Style Sheet,
linktitle: SCSS
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ SCSS และ API ที่สามารถสร้างและเปิดไฟล์ SCSS"
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## ไฟล์ SCSS คืออะไร?? ##

SCSS เป็นไวยากรณ์ที่สองของ Sass (Syntactically Awesome Stylesheet) ที่ใช้วงเล็บเหลี่ยมแทนการเยื้อง SCSS ได้รับการออกแบบในลักษณะที่ไฟล์ CSS3 ที่ถูกต้องเป็นไฟล์ SCSS ที่ถูกต้องด้วย ไฟล์ SCSS ถูกจัดเก็บด้วยนามสกุล .scss

## ทำไมต้องใช้ SCSS ##

เนื่องจากการออกแบบเว็บไซต์มีความซับซ้อน ส่งผลให้มีไฟล์ [CSS](/th/web/css/) ขนาดใหญ่ ไฟล์ดังกล่าวดูแลรักษายากกว่า นี่คือที่มาของ SCSS SCSS แนะนำตัวแปร การซ้อน การผสม การนำเข้า และการสืบทอดตัวเลือกในการพัฒนา CSS ส่วนเพิ่มเติมเหล่านี้ทำให้การทำงานออกแบบสนุกขึ้นมาก

## วิธีใช้ไฟล์ SCSS ##

ไฟล์ SCSS ไม่ได้รวมอยู่ในเอกสาร [HTML](/th/web/html/) โดยตรง เช่น CSS ไฟล์ SCSS จะถูกแปลงเป็นไฟล์ CSS ที่รวมอยู่ในไฟล์ HTML แทน หากต้องการติดตั้ง SCSS ในระบบของคุณ ให้ทำตามคำแนะนำที่ให้ไว้ใน [ไซต์ Sass อย่างเป็นทางการ] (https://sass-lang.com/install)
หากต้องการแปลง SCSS เป็น CSS คุณอาจแปลงไฟล์ SCSS ที่บันทึกไว้แล้วหรือเฝ้าดูการเปลี่ยนแปลงและแปลงเมื่อบันทึกไฟล์แล้ว คำสั่งสำหรับทั้งสองได้รับด้านล่าง

### แปลงครั้งเดียว ###

พารามิเตอร์แรกคือไฟล์ SCSS ต้นทาง และพารามิเตอร์ที่สองคือไฟล์ CSS เอาต์พุต

```cmd
sass main.scss main.css
```

### เฝ้าดูการเปลี่ยนแปลง ###

คำสั่งมีแฟล็ก *watch** เพิ่มเติมที่ทำให้คำสั่งทำงานต่อไป และทันทีที่บันทึกไฟล์ SCSS เอาต์พุต CSS จะถูกสร้างขึ้น

```cmd
sass --watch main.scss main.css
```

## ไวยากรณ์ SCSS ##

SCSS รองรับตัวแปร, การซ้อน, มิกซ์อิน, อิมพอร์ต, การสืบทอดตัวเลือก ฯลฯ ด้านล่างนี้เป็นตัวอย่างของคุณสมบัติเหล่านี้

### ตัวแปร ###

ด้วยการใช้ตัวแปร คุณสามารถตั้งค่าข้อมูลที่นำมาใช้ซ้ำได้ เช่น สีหลักหรือสีพื้นหลังสำหรับปุ่มบันทึก สิ่งนี้มีประโยชน์หากคุณต้องการเปลี่ยนแปลงข้อมูลนั้น คุณเพียงแค่เปลี่ยนที่ตำแหน่งเดียวและจะอัปเดตทุกที่ที่มีการใช้งาน

**สคส**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

คุณสามารถซ้อนตัวเลือก CSS คล้ายกับลำดับชั้นของ HTML ในตัวอย่างด้านล่าง สแปนซ้อนอยู่ภายในบล็อก h1

**สคส**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

มิกซ์อินสามารถใช้เพื่อจัดกลุ่มคุณสมบัติที่คล้ายกันซึ่งใช้ร่วมกันในหลายๆ ที่ คุณยังสามารถส่งพารามิเตอร์ไปยังมิกซ์อิน

**สคส**

**ประกาศผสม**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**ใช้มิกซ์อิน**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
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

การขยาย/การสืบทอดมีประโยชน์ในกรณีที่จำเป็นต้องแชร์คุณสมบัติของตัวเลือกหนึ่งกับตัวเลือกอื่น ในตัวอย่างด้านล่าง ตัวเลือก *.error-notice* ใช้คุณสมบัติทั้งหมดของตัวเลือก *.error-text* และเพิ่มคุณสมบัติเส้นขอบและการเติม

**สคส**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
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

การนำเข้าจะมีประโยชน์ในการแยกข้อกังวล คุณอาจแบ่งลักษณะในลักษณะที่ลักษณะส่วนหัวอยู่ในไฟล์แยกต่างหาก ลักษณะส่วนท้ายอยู่ในไฟล์แยกต่างหาก ตัวแปรสีทั้งหมดที่ใช้ในรูปแบบสามารถอยู่ในไฟล์แยกต่างหาก เป็นต้น การใช้เทคนิคนี้ รูปแบบอยู่เป็นระเบียบ คุณเพียงแค่นำเข้าไฟล์ในไฟล์ SCSS หลักตามที่แสดงในตัวอย่างด้านล่าง คุณไม่จำเป็นต้องระบุนามสกุลไฟล์ในคำสั่งนำเข้า Sass รวบรวมไฟล์ SCSS ทั้งหมดโดยตรง หากต้องการหลีกเลี่ยงการคอมไพล์ไฟล์อิมพอร์ตโดยตรง คุณสามารถทำให้ไฟล์เหล่านี้บางส่วนโดยเพิ่มเครื่องหมายขีดล่าง (_) ก่อนชื่อไฟล์ คุณสามารถนำเข้าบางส่วนที่คล้ายกับไฟล์ SCSS ทั่วไปโดยไม่ต้องขีดล่าง

**สคส**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

CSS เอาต์พุตจะมีสไตล์จากไฟล์ที่นำเข้าทั้งหมด

## อ้างอิง ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

