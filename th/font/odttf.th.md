{
  "date": "2023-01-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ไฟล์ ODTTF - รูปแบบไฟล์ฟอนต์ OpenType ที่สร้างความสับสน",
  "description": "เรียนรู้เกี่ยวกับรูปแบบไฟล์ ODTTF และ API ที่สามารถสร้างและเปิดไฟล์ ODTTF",
  "linktitle": "ODTTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-odtt-thf"
}
},
  "lastmod": "2023-01-13"
}

## ไฟล์ ODTTF คืออะไร??

An ODTTF file is a font file format that is utilized by the [.XPS](/page-description-language/xps/) and Microsoft Office 2007 file formats. It contains obfuscated OpenType font that has been modified in order to make it difficult to extract the font's design information or to reverse-engineer the font's source code. ODTTF is based on the fonts used in the original documents but are not in plain format and may not be to read by third-party software to extract font data.

คุณสามารถเปิดไฟล์ ODTTF โดยใช้ Pagemark XpsViewer, Apple Safari พร้อม Pagemark XpsPlugin, Mozilla Firefox พร้อม Pagemark XpsPlugin,
มุมมอง NiXPS และการแก้ไข NiXPS

## รูปแบบไฟล์ ODTTF

โครงสร้างรูปแบบไฟล์ภายในของรูปแบบไฟล์ ODTTF ไม่เป็นที่รู้จักเนื่องจากโครงสร้างเหล่านี้ถูกจัดเก็บเป็นรูปแบบที่สับสนแบบฝัง สิ่งเหล่านี้สามารถฝังอยู่ในเอกสารดิจิทัล เช่น .PDF หรือ .DOCX

