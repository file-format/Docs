{
  "date" : "2021-05-24",
  "keywords" :["xul", "File", "Extension", "File Format", "File Extension", "XML User Interface Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - ไฟล์ภาษาส่วนต่อประสานผู้ใช้ XML",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ XUL และ API ที่สามารถสร้างและเปิดไฟล์ XUL",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## ไฟล์ XUL คืออะไร??

ไฟล์ที่มีนามสกุล .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) ย่อมาจาก XML User Interface Language) เป็นไฟล์ภาษามาร์กอัปที่ใช้ [XML](/th/web/xml/) สำหรับ การสร้างส่วนติดต่อผู้ใช้ ได้รับการพัฒนาโดย Mozilla เพื่อให้นักพัฒนาสร้างองค์ประกอบส่วนติดต่อผู้ใช้แบบกราฟิกที่คล้ายกับภาษามาร์กอัปอื่น ๆ ที่ใช้สำหรับสร้างหน้าเว็บ XUL ได้รับการใช้งานอย่างกว้างขวางโดย Mozilla ในเบราว์เซอร์ Firefox ซึ่งใช้ Mozilla codebase การแสดงผล XUL ดำเนินการโดยใช้
[เครื่องยนต์ Gecko](https://en.wikipedia.org/wiki/Gecko_(software)) ส้อมของ Firefox เช่น Pale Moon, Basilisk และ Waterfox ยังคงรองรับโปรแกรมเสริม XUL ไฟล์ XUL ถูกระบุด้วยประเภท MIME: application/vnd.mozilla.xul+xml

## รูปแบบไฟล์ XUL

ไฟล์ XUL เขียนด้วยข้อความธรรมดาตามรูปแบบไฟล์ XML และแสดงผลโดยใช้เอ็นจิ้น Gecko สามส่วนหลักของโครงสร้าง XUL คือ:

* `เนื้อหา` - รวมถึงการประกาศของหน้าต่างและองค์ประกอบส่วนต่อประสานผู้ใช้ที่อยู่ภายใน
* `Skin` - ประกอบด้วยสไตล์ชีต รูปภาพ และไฟล์ที่เกี่ยวข้องกับธีมอื่นๆ ลักษณะที่ปรากฏของหน้าต่างอธิบายไว้ในสไตล์ชีต
* `Locale` - ข้อความที่แสดงภายในหน้าต่างจะถูกจัดเก็บแยกกัน และผู้ใช้สามารถใช้ไฟล์ภาษาได้หลายชุด

### ตัวอย่าง XUL

ตัวอย่างต่อไปนี้สร้างปุ่มสามปุ่มที่วางซ้อนกันในแนวตั้ง

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3....",
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## อ้างอิง

* [XUL - โดย Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [เอกสารที่เก็บถาวร XUL - โดย Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

