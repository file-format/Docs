{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ FZP และ API ที่สามารถสร้างและเปิดไฟล์ FZP",
  "title" :"รูปแบบไฟล์ FZP - ไฟล์คำอธิบายส่วน Fritzing XML",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## ไฟล์ FZP คืออะไร??

ไฟล์ FZP เป็นไฟล์ XML ที่สร้างขึ้นโดยแอปพลิเคชันการสร้างต้นแบบและออกแบบวงจรอิเล็กทรอนิกส์ [Fritzing](https://fritzing.org/) ประกอบด้วยข้อมูลเกี่ยวกับคุณสมบัติของชิ้นส่วน ตัวเชื่อมต่อ และบัสในรูปแบบไฟล์ [XML](/th/web/xml/) ไม่สามารถใช้ไฟล์ FPZ ได้อย่างอิสระใน Fritzing แต่จะถูกนำเข้าเป็นส่วนหนึ่งของไฟล์เก็บถาวร FZPZ

## รูปแบบไฟล์ FZP - ข้อมูลเพิ่มเติม

ไฟล์ FZP เป็นไฟล์ XML ที่มีข้อมูลเกี่ยวกับคุณสมบัติของชิ้นส่วน ตัวเชื่อมต่อ และบัส นอกจากนี้ ไฟล์ FZP ยังมีข้อมูลเกี่ยวกับชื่อ คำอธิบาย ผู้แต่ง และวันที่เผยแพร่ไฟล์ FZP เมื่อส่งออกไฟล์ส่วน Fritzing แอป Fritzing จะสร้างไฟล์เก็บถาวรแบบบีบอัด [FZPZ](/th/compression/fzpz/) ที่มีไฟล์ FZP และไฟล์ [SVG](/th/page-description-language/svg/) สี่ไฟล์

[ข้อกำหนดรูปแบบไฟล์ FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) มีอยู่ใน Github โดย Fritzing

## ตัวอย่างโครงสร้างไฟล์ FZP

ไฟล์ FZP ทั่วไปมีโครงสร้าง XML ดังต่อไปนี้

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>,
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## อ้างอิง

* [ข้อกำหนดรูปแบบไฟล์ FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [ส่วนใหม่พร้อมส่วนขยาย fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

