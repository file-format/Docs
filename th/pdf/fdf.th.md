{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ FDF - ไฟล์ FDF คืออะไร",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ FDF และ API ที่สามารถสร้างและเปิดไฟล์ FDF",
  "linktitle" : "FDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ FDF คืออะไร??

ไฟล์ FDF (**Forms Data Format**) คือเอกสารข้อความที่สร้างขึ้นโดยการส่งออกข้อมูลจากช่องแบบฟอร์มของไฟล์ [PDF](/th/pdf/) โดยจะรวมเฉพาะข้อมูลช่องข้อความที่ดึงมาจากช่องแบบฟอร์มที่มีอยู่ในไฟล์ PDF ส่งผลให้ไฟล์ข้อมูลมีขนาดเล็กเนื่องจากข้อมูลที่ส่งออกไม่มีฟอร์ม Adobe Acrobat มีคุณสมบัติในการส่งออกข้อมูลช่องแบบฟอร์มโดยใช้ตัวเลือก 'ส่งออกข้อมูลแบบฟอร์ม' จากเมนูแอปพลิเคชัน

## รูปแบบไฟล์ FDF - ข้อมูลเพิ่มเติม

FDF เป็นรูปแบบข้อความล้วนและรวมอยู่ใน [มาตรฐาน ISO 32000](https://www.iso.org/standard/51502.html) สำหรับรูปแบบเอกสารพกพา ได้รับการพัฒนาโดย Adobe เพื่อให้นำเข้าและส่งออกข้อมูลจาก Acrobat Forms หรือ AcroForms

ไฟล์ FDF มีสองประเภท:

• `Classic FDF` – ให้ข้อมูลเพื่อกรอกแบบฟอร์มคงที่ที่มีอยู่

• `เทมเพลต FDF` – สร้าง PDF ใหม่ตามเทมเพลตจากไฟล์ PDF ที่ระบุภายใน แบบฟอร์มภายในเอกสารใหม่กรอกโดยการให้ข้อมูล

## การสร้าง FDF โดยใช้ Adobe Acrobat

[ชุดเครื่องมือ FDF](https://opensource.adobe.com/dc-acrobat-sdk-docs/) จาก Adobe ช่วยให้คุณสร้างไฟล์ FDF จากข้อมูลข้อความได้

## อ้างอิง ##

* [รองรับรูปแบบ FDF โดย Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)
* [แหล่งข้อมูลสำหรับนักพัฒนาซอฟต์แวร์ของ Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

