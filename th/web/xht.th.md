{
  "date" : "2021-05-24",
  "keywords" :["xht", "File", "Extension", "File Format", "File Extension", "extended hypertext markup language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"เอ็กซ์เอชที",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ XHT และ API ที่สามารถสร้างและเปิดไฟล์ XHT",
  "linktitle" : "XHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## ไฟล์ XHT คืออะไร??

ไฟล์ที่มีนามสกุล .xht คือไฟล์เว็บที่เกี่ยวข้องกับประเภทไฟล์ [XHTML](/th/web/xhtml/) (Extended Hypertext Markup Language) ซึ่งตัวมันเองเป็นไฟล์มาร์กอัปที่ใช้ [XML](/th/web/xml/) ไฟล์ทั้งสองนี้คล้ายกับ HTML แต่มีไวยากรณ์คล้าย XML ที่เข้มงวดกว่า ไฟล์ XHT ได้รับการออกแบบให้มีโครงสร้างมากขึ้น ใช้สคริปต์น้อยลง และเป็นไฟล์ทั่วไปนอกเหนือจากการใช้สิ่งอำนวยความสะดวกที่มีอยู่ของ XML

## รูปแบบไฟล์ XHT

ไฟล์ XHT ถูกสร้างขึ้นและจัดเก็บเป็นไฟล์ข้อความธรรมดาที่มีการเข้ารหัส UTF-8 ตามค่าเริ่มต้น ประกอบด้วยซอร์สโค้ดที่สมบูรณ์ของเอกสาร XHTML ที่สามารถเปิดและแก้ไขได้ด้วยโปรแกรมแก้ไขข้อความที่รองรับการเข้ารหัส Unicode นอกจากโปรแกรมแก้ไขข้อความแล้ว รูปแบบไฟล์ XHT ยังเป็นที่เข้าใจได้โดยเว็บเบราว์เซอร์สมัยใหม่ส่วนใหญ่และสามารถเปิดได้โดยใช้สิ่งเหล่านี้

## ตัวอย่าง XHT

ตัวอย่างเอกสาร XHT ต่อไปนี้กำหนดการประกาศ XML

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>,
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

## อ้างอิง ##

* [ประวัติของ XHTML: จากปี 1990 ถึงปัจจุบัน](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

