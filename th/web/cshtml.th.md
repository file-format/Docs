{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml","ไฟล์ cshtml", "รูปแบบไฟล์ cshtml", "ประเภทไฟล์ cshtml", "ไฟล์", "ประเภท", "ไฟล์ cshtml คืออะไร" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - เว็บเพจมีดโกน ASP.NET",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CSHTML และ API ที่สามารถสร้างและเปิดไฟล์ CSHTML",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## ไฟล์ CSHTML คืออะไร?

ไฟล์ที่มีนามสกุล .cshtml คือไฟล์ HTML [C#](/th/programming/cs/) ซึ่งใช้ที่ฝั่งเซิร์ฟเวอร์โดยเครื่องมือ Razor Markup เพื่อแสดงไฟล์หน้าเว็บไปยังเบราว์เซอร์ของผู้ใช้ การเข้ารหัสฝั่งเซิร์ฟเวอร์นี้คล้ายกับเพจ ASP.NET มาตรฐาน ทำให้สามารถสร้างเนื้อหาเว็บแบบไดนามิกได้ทันทีเนื่องจากเว็บเพจถูกเขียนไปยังเบราว์เซอร์ เซิร์ฟเวอร์ดำเนินการโค้ดฝั่งเซิร์ฟเวอร์ภายในหน้าก่อนที่จะส่งหน้าที่สร้างขึ้นไปยังเบราว์เซอร์ งานที่ซับซ้อน เช่น การเข้าถึงฐานข้อมูลและการแสดงผลมุมมองที่ซับซ้อน ไฟล์ CSHTML สามารถสร้างและตั้งโปรแกรมโดยใช้ Microsoft Visual Studio

## รูปแบบไฟล์ CSHTML

ไฟล์ CSHTML เป็นไฟล์ข้อความที่เป็นไปตามไวยากรณ์ที่ระบุโดยเครื่องมือมาร์กอัปของ Razor Razor รองรับทั้ง C# และ VB.NET และเรียนรู้และใช้งานได้ง่ายกว่า ASP และ ASP.NET แบบคลาสสิก w3schools มีคำแนะนำที่เรียบง่ายแต่มีประสิทธิภาพสำหรับ [ไวยากรณ์ของ C# และ VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) การเข้ารหัสของ Razor

### ตัวอย่าง CSHTML

ต่อไปนี้เป็นตัวอย่างโค้ด C# ที่ใช้ในไฟล์ CSHTML สำหรับ Razor

```
<!-- Single statement block -->
@{ var myMessage = "Hello World"; }

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@{
var greeting = "Welcome to our site!";
var weekDay = DateTime.Now.DayOfWeek;
var greetingMessage = greeting + " Here in Huston it is: " + weekDay;
}
<p>The greeting is: @greetingMessage</p>
```

รหัส VB.NET ที่เทียบเท่าสำหรับ Razor มีดังต่อไปนี้

```
<!-- Single statement block  -->
@Code dim myMessage = "Hello World" End Code

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@Code
dim greeting = "Welcome to our site!"
dim weekDay = DateTime.Now.DayOfWeek
dim greetingMessage = greeting & " Here in Huston it is: " & weekDay
End Code

<p>The greeting is: @greetingMessage</p>
```

## อ้างอิง

* [การอ้างอิงไวยากรณ์ของ Razor - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

