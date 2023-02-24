{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ XFDF - ไฟล์ XFDF คืออะไร",
  "description":"เรียนรู้เกี่ยวกับไฟล์ XFDF และ API ที่สามารถสร้างและเปิดไฟล์ XFDF",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ XFDF คืออะไร??

ไฟล์ที่มีนามสกุล .xfdf เป็นรูปแบบข้อมูล XML Forms ที่สร้างขึ้นด้วยซอฟต์แวร์ Adobe Acrobat เช่นเดียวกับ [FDF](/th/pdf/fdf/) XFDF มีคำอธิบายองค์ประกอบของฟอร์มและค่าในรูปแบบ XML ซึ่งอาจรวมถึงชื่อและค่าของช่องข้อความในแบบฟอร์ม PDF XFDF ถูกบันทึกในรูปแบบที่มนุษย์อ่านได้และสามารถอ่านแบบโปรแกรมได้โดยใช้ภาษาโปรแกรม เช่น C#

## รูปแบบไฟล์ XFDF - ข้อมูลเพิ่มเติม

ไฟล์ XFDF ถูกบันทึกในรูปแบบไฟล์ XML ซึ่งเป็นรูปแบบสากลที่ใช้สำหรับนำเข้าและส่งออกข้อมูล โครงสร้างไฟล์ XFDF ประกอบด้วยส่วนหัว ตามด้วยค่าฟิลด์ และข้อมูลองค์ประกอบดังที่แสดงด้านล่าง

|องค์ประกอบ|แอตทริบิวต์|เนื้อหา|
---|---|---|
|\<XFDF> ||องค์ประกอบบนสุด|
|\<fields> ||ค่าฟิลด์ทั้งหมดสำหรับเทมเพลตนี้|
|<field (T)> |ชื่อ |ชื่อฟิลด์|
|<value (V)> |ค่า |ค่าฟิลด์|

## อ้างอิง

* [รองรับรูปแบบ FDF โดย Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [แหล่งข้อมูลสำหรับนักพัฒนาซอฟต์แวร์ของ Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

