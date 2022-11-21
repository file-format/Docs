{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "extension", "file", "file format", "Database File Type", "Database File Format", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ ADE และ API ที่สามารถสร้างและเปิดไฟล์ ADE",
  "title" :"ADE - ไฟล์ส่วนขยายโครงการ Access",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## ไฟล์ ADE คืออะไร??

ไฟล์ที่มีนามสกุล .ade คือไฟล์โครงการ Microsoft Access ที่มีเอาต์พุตที่คอมไพล์แล้วของข้อมูลที่มีอยู่ในไฟล์โครงการ Microsoft Access ADP ข้อมูลในไฟล์โครงการ Access นอกเหนือจาก Visual Basic for Applications (VBA) จะพร้อมใช้งานในรูปแบบที่คอมไพล์แล้วในไฟล์ ADE ข้อมูลถูกจัดเก็บในรูปแบบบีบอัดในไฟล์เหล่านี้เพื่อลดขนาดไฟล์และปรับปรุงประสิทธิภาพการทำงานใน Access เนื่องจาก ADE เป็นเอาต์พุตที่คอมไพล์แล้วของไฟล์โครงการ Access ซอร์สโค้ด VBA ใดๆ ที่เป็นส่วนหนึ่งของโครงการจึงยังคงได้รับการปกป้องโดยไม่อนุญาตให้เป็นส่วนหนึ่งของเอาต์พุต ไฟล์ ADE สามารถเปิดได้ใน Microsoft Access 365

## รูปแบบไฟล์ ADE - ข้อมูลเพิ่มเติม

ADE จะรวบรวมไฟล์ฐานข้อมูล Access ที่จัดเก็บไว้ในดิสก์เป็นไฟล์ไบนารี ไม่รู้จักโครงสร้างไฟล์ภายในของไฟล์เหล่านี้

ไฟล์ ADE สามารถสร้างปัญหาในการเปิดตามเวอร์ชันของ Microsoft Access ที่ใช้สร้างไฟล์เหล่านี้ ฐานข้อมูล Access ที่ใช้ Microsoft Access 2010 รุ่น 64 บิต และคอมไพล์เป็นไฟล์ MDE, [ACCDE](/th/database/accde/) หรือ ADE จะต้องคอมไพล์ใหม่ใน Microsoft Access 2021 Service Pack 1 (SP1) เพื่อ ทำงานอย่างถูกต้องกับ Access 2010 SP1 ปัญหานี้เกิดขึ้นเนื่องจาก Access 2010 SP1 ใช้ไฟล์ VBE7.dll เวอร์ชันที่ใหม่กว่า (เวอร์ชัน 7.00.1619)

## อ้างอิง

* [ปัญหาเกี่ยวกับไฟล์ Access ADE](https://docs.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [รูปแบบไฟล์ Access ใดที่จะใช้](https://support.microsoft.com/en-us/office/ which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

