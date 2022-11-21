{
  "date" : "2021-01-20",
  "keywords" :["xslt", "File", "Extensible", "File Format", "File Extension", "Extensible Stylesheet Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ XSLT",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ XSLT และ API ที่สามารถสร้างและเปิดไฟล์ XSLT",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## ไฟล์ XSLT คืออะไร??

ไฟล์ที่มีนามสกุล .xslt คือไฟล์ Extensible Stylesheet Language Transformation ที่ใช้ในการแปลงและจัดรูปแบบไฟล์ XML โดยใช้คำสั่ง XSL รูปแบบนี้ใช้เพื่อแปลงเอกสาร XML เป็นรูปแบบเอาต์พุตมาตรฐาน เช่น เอกสารข้อความหรือเว็บเพจ .html การแปลงนี้สร้างเอกสารใหม่ตามเนื้อหาของเอกสาร XML ที่มีอยู่ XSLT ทำให้สามารถคำนวณได้ตามอำเภอใจในทางทฤษฎี

## รูปแบบไฟล์ XSLT

รูปแบบไฟล์ XLST มีคำแนะนำการแปลงในรูปแบบข้อความธรรมดาที่สามารถดูได้ในโปรแกรมแก้ไขข้อความใดๆ มีการแก้ไขภาษาสามครั้ง

* `XSLT 1.0` - XSLT 1.0 เผยแพร่เป็นคำแนะนำของ W3C ในเดือนพฤศจิกายน 1999
* `XSLT 2.0` - ประกอบด้วยการแก้ไข เช่น การจัดการสตริงโดยใช้นิพจน์ทั่วไป ฟังก์ชันและตัวดำเนินการสำหรับการจัดการวันที่ เวลา และระยะเวลา เอกสารเอาต์พุตหลายรายการ การจัดกลุ่ม และระบบประเภทที่สมบูรณ์ยิ่งขึ้นและการตรวจสอบประเภทที่แข็งแกร่ง
* `XSLT 3.0` - กลายเป็นส่วนหนึ่งของ W3C Recommendation เมื่อวันที่ 8 มิถุนายน 2017 และคุณสมบัติหลักใหม่ ได้แก่ การแปลงสตรีมมิ่ง แพ็คเกจเพื่อปรับปรุงความเป็นโมดูลาร์ของสไตล์ชีตขนาดใหญ่ การจัดการข้อผิดพลาดแบบไดนามิกที่ปรับปรุงด้วย ตัวอย่างเช่น คำสั่ง xsl:try และรองรับแผนที่และอาร์เรย์ ทำให้ XSLT สามารถจัดการ JSON และ XML ได้

### ตัวอย่าง XSLT

ตัวอย่างต่อไปนี้นำมาจาก [w3schools](https://www.w3schools.com/xml/xsl_intro.asp)
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>,
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## อ้างอิง ##

* [XSLT - โดย Wikipedia](https://en.wikipedia.org/wiki/XSLT)
* [องค์ประกอบ XSLT](https://en.wikipedia.org/wiki/XSLT_elements)

