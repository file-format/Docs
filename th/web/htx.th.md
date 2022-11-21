{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ HTX - รูปแบบไฟล์นามสกุล HTML",
  "description" :"คู่มือรูปแบบไฟล์ของคุณเพื่อเรียนรู้ว่าไฟล์ HTX และ API ใดที่สามารถสร้างและเปิดไฟล์ HTX ได้",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ HTX คืออะไร??

ไฟล์ HTX เป็นไฟล์ HTML ที่มีตัวแปรข้อมูลสำหรับแสดงผลการสืบค้นฐานข้อมูลในรูปแบบเว็บเพจ ส่วนใหญ่สร้างขึ้นด้วยซอฟต์แวร์พัฒนาเว็บ Microsoft FrontPage ไฟล์ HTX จะถูกบันทึกไว้ในโฟลเดอร์เดียวกันกับไฟล์ Internet Database Connector (.IDC) ที่สอดคล้องกัน

ไฟล์ HTX สามารถเปิดได้ด้วยแอปพลิเคชัน เช่น Microsoft FrontPage และโปรแกรมแก้ไขข้อความใดๆ เช่น Notepad, TextEdit หรือ Atom

## รูปแบบไฟล์ HTX

ไฟล์ HTX จะถูกบันทึกเป็นไฟล์ข้อความธรรมดาพร้อมรหัสสำหรับดึงข้อมูลจากฐานข้อมูลและบันทึกในตัวแปรสำหรับแสดงผล


### ตัวอย่างไฟล์ HTX

ตัวอย่างของไฟล์ HTX มีดังต่อไปนี้ซึ่งกำหนดส่วนหัวของเพจสำหรับแสดงข้อจำกัดการสืบค้นและเอกสารที่แสดงบนเพจเพื่อแสดงต่อผู้ใช้

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

ผลลัพธ์ของโค้ดตัวอย่างนี้มีดังต่อไปนี้

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

อย่างที่คุณเห็น ไฟล์ HTX เป็นเทมเพลตที่จัดรูปแบบวิธีการส่งคืนและแสดงผลลัพธ์ต่อผู้ใช้ปลายทาง มันถูกเขียนในรูปแบบ HTML พร้อมส่วนขยาย IIS และ Indexing Service ส่วนขยายเหล่านี้รวมถึงชื่อตัวแปรและรหัสอื่นๆ สำหรับการประมวลผลผลลัพธ์

## อ้างอิง

* [การจัดรูปแบบผลลัพธ์เป็นไฟล์ .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

