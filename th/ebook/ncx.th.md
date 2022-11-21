{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "ไฟล์ XML การควบคุมการนำทางของ EPUB", "นามสกุล", "รูปแบบ", "E-Book", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ XML การควบคุมการนำทางของ EPUB (NCX) และ API ที่สามารถสร้างและเปิดไฟล์ NCX",
  "title" :"NCX - ไฟล์ XML ควบคุมการนำทาง EPUB",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## ไฟล์ NCX คืออะไร?? ##

ไฟล์ NCX เรียกโดยย่อว่าเป็นไฟล์ควบคุมการนำทางสำหรับ XML ซึ่งโดยปกติจะมีชื่อว่า toc.ncx ไฟล์นี้ประกอบด้วยสารบัญลำดับชั้นสำหรับไฟล์ EPUB ข้อมูลจำเพาะสำหรับ NCX ได้รับการพัฒนาสำหรับ Digital Talking Book (DTB) และรูปแบบไฟล์นี้ได้รับการดูแลโดย **DAISY Consortium** และไม่เป็นส่วนหนึ่งของข้อกำหนดของ EPUB ไฟล์ NCX มี **application/x-dtbncx+xml** ประเภท mime อยู่ด้วย

## สเปค NCX ##

ไฟล์ NCX มีแท็ก XML หลายประเภท เมตาแท็ก เช่น `meta name="dtb:uid"` ใช้เพื่อกล่าวถึง ID องค์ประกอบ `meta name="dtb:ความลึก"` ถูกตั้งค่าให้เท่ากับความลึกขององค์ประกอบแท็ก `navMap` องค์ประกอบ `navPoint` สามารถซ้อนกันเพื่อสร้างสารบัญแบบลำดับชั้น เนื้อหาของ `navLabel` คือข้อความที่ปรากฏในสารบัญที่สร้างโดยระบบการอ่านที่ใช้ .ncx เนื้อหาขององค์ประกอบ `navPoint` ชี้ไปที่เอกสารเนื้อหาที่แสดงอยู่ในรายการ และยังสามารถรวมตัวระบุองค์ประกอบ

คำอธิบายข้อยกเว้นบางประการสำหรับข้อกำหนดเฉพาะของ NCX ที่ใช้ใน EPUB คุณสามารถดูตัวอย่างไฟล์ NCX ได้ที่นี่:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ncx PUBLIC "-//NISO//DTD ncx 2005-1//EN"
"http://www.daisy.org/z3986/2005/ncx-2005-1.dtd">

<ncx version="2005-1" xml:lang="en" xmlns="http://www.daisy.org/z3986/2005/ncx/">

  <head>
<!-- The following four metadata items are required for all NCX documents,
including those that conform to the relaxed constraints of OPS 2.0 -->

    <meta name="dtb:uid" content="123456789X"/> <!-- same as in .opf -->
    <meta name="dtb:depth" content="1"/> <!-- 1 or higher -->
    <meta name="dtb:totalPageCount" content="0"/> <!-- must be 0 -->
    <meta name="dtb:maxPageNumber" content="0"/> <!-- must be 0 -->
  </head>

  <docTitle>
    <text>Pride and Prejudice</text>
  </docTitle>

  <docAuthor>
    <text>Austen, Jane</text>
  </docAuthor>

  <navMap>
    <navPoint class="chapter" id="chapter1" playOrder="1">
      <navLabel><text>Chapter 1</text></navLabel>
      <content src="chapter1.xhtml"/>
    </navPoint>
  </navMap>

</ncx>
```

## อ้างอิง ##

* [EPUB จาก Wikipedia](https://en.wikipedia.org/wiki/EPUB)
* [ไฟล์อะไรที่จะรวมไว้ใน toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

