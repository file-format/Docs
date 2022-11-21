{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ RST- ไฟล์ reStructuredText",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ RST และ API ที่สามารถสร้างและเปิดไฟล์ RST",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## ไฟล์ RST คืออะไร??

ไฟล์ RST เป็นรูปแบบไฟล์เอกสารทางเทคนิค ซึ่งใช้ในชุมชนโปรแกรม Python เป็นหลัก เป็นไฟล์ข้อความที่เขียนด้วยภาษามาร์กอัป reStructuredText ที่ใช้สไตล์และการจัดรูปแบบกับเอกสารข้อความธรรมดาสำหรับการสร้างเอกสารประกอบ ไฟล์ RST ใช้ความคิดเห็นและข้อมูลอื่น ๆ ในรหัสโปรแกรม Python เพื่อสร้างเอกสารทางเทคนิคของแอปพลิเคชัน อย่างไรก็ตาม ข้อความเหล่านี้อาจมีข้อความที่แปลงเป็นหน้าเว็บและ [eBooks](/th/ebook/) ได้ด้วย สามารถใช้โปรแกรมแก้ไขข้อความเช่น Github Atom, GNU Emacs (ข้ามแพลตฟอร์ม), Microsoft Notepad (Windows), Apple TextEdit (Mac) และ Vim (Linux) เพื่อเปิดไฟล์ RST

## รูปแบบไฟล์ RST

ไฟล์ RST มีรหัสที่เขียนด้วยภาษามาร์กอัป reStructuredText เป็นส่วนหนึ่งของโครงการ Docutils ของ Python Doc-SIG (Documentation Special Interest Group) ซึ่งมีชุดเครื่องมือสำหรับ Python คล้ายกับ Javadoc สำหรับ Java ตัวแยกวิเคราะห์สำหรับรูปแบบไฟล์ RST นั้นฝังอยู่ใน Docutils และสามารถดึงข้อมูลจากโปรแกรม Python เพื่อจัดรูปแบบให้เป็นเอกสารประกอบของโปรแกรม

### ตัวอย่าง reStructuredText RST

ให้ยกตัวอย่างข้อความที่เขียนในรูปแบบไฟล์ RST ดังนี้

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

เมื่อป้อนข้อความนี้ไปยังตัวประมวลผล rST เช่น Docutils ผลลัพธ์จะเป็นดังนี้

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## อ้างอิง ##

* [reStructuredText - โดย Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)

