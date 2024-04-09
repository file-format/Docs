{
  "date" : "2019-10-11",
  "keywords" :["xml", "ไฟล์", "นามสกุล", "รูปแบบไฟล์", "นามสกุลไฟล์", "ภาษามาร์กอัปที่ขยายได้"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ XML",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ XML และ API ที่สามารถสร้างและเปิดไฟล์ XML",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ XML คืออะไร?

XML ย่อมาจาก Extensible Markup Language ซึ่งคล้ายกับ **[HTML](/th/web/html/)** แต่แตกต่างกันที่การใช้แท็กสำหรับกำหนดวัตถุ แนวคิดทั้งหมดที่อยู่เบื้องหลังการสร้างรูปแบบไฟล์ XML คือการจัดเก็บและส่งข้อมูลโดยไม่ต้องพึ่งพาเครื่องมือซอฟต์แวร์หรือฮาร์ดแวร์ ความนิยมของมันเกิดจากการที่มันสามารถอ่านได้ทั้งมนุษย์และเครื่อง สิ่งนี้ทำให้สามารถสร้างโปรโตคอลข้อมูลทั่วไปในรูปแบบของอ็อบเจกต์ที่จะจัดเก็บและแชร์ผ่านเครือข่าย เช่น เวิลด์ไวด์เว็บ (WWW) "X" ใน XML ใช้สำหรับขยายได้ ซึ่งหมายความว่าภาษาสามารถขยายเป็นสัญลักษณ์จำนวนเท่าใดก็ได้ตามความต้องการของผู้ใช้ รูปแบบไฟล์มาตรฐานจำนวนมากใช้ประโยชน์จากคุณสมบัติเหล่านี้ เช่น Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/th/web/xhtml/)** และ **[SVG](/th/page-description-language/svg/)**.

## รูปแบบไฟล์ XML

รูปแบบไฟล์ XML อ้างอิงจาก XML Document Object Model (DOM) ซึ่งเป็น API การเขียนโปรแกรมสำหรับเอกสาร HTML และ XML XML DOM กำหนดวิธีการมาตรฐานในการเข้าถึงและจัดการองค์ประกอบเอกสาร XML สร้างมุมมองโครงสร้างแบบต้นไม้ของเอกสาร XML ที่สามารถใช้เพื่อเข้าถึงองค์ประกอบทั้งหมดผ่านแผนผัง DOM องค์ประกอบที่มีอยู่สามารถแก้ไข/ลบได้ รวมทั้งสามารถสร้างองค์ประกอบใหม่ในแผนผัง XML แต่ละองค์ประกอบของเอกสาร XML เรียกว่าโหนด XML DOM แสดงดังภาพต่อไปนี้

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### แนวทางสากลของ XML

พลังของ XML ทำให้เป็นภาษาสากลสำหรับการสื่อสารข้อมูลผ่านเครือข่ายโดยทำให้การขนส่งข้อมูลและการเปลี่ยนแปลงแพลตฟอร์มง่ายขึ้น นอกจากนี้ยังทำให้แน่ใจว่าสามารถแลกเปลี่ยนข้อมูลระหว่างระบบที่เข้ากันไม่ได้ด้วยการจัดเก็บข้อมูลในรูปแบบข้อความล้วน HTML ใช้สำหรับการแสดงข้อมูลบนเว็บ ในขณะที่ XML ใช้สำหรับการแลกเปลี่ยนข้อมูล คู่แท็กมาร์กอัปที่ใช้ภายใน XML กำหนดองค์ประกอบหลักของโครงสร้างที่จะใช้โดยการอ่านแอปพลิเคชัน

## ตัวอย่าง XML

ต่อไปนี้คือตัวอย่างง่ายๆ ของแค็ตตาล็อกซีดีที่แต่ละระเบียนมีข้อมูลเกี่ยวกับซีดี เช่น ศิลปิน ประเทศ บริษัท ราคา และปีที่ผลิต

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## อ้างอิง

* [XML - โดย Wikipedia](https://en.wikipedia.org/wiki/XML)

