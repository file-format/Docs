{
  "date" : "2022-01-04",
  "keywords" :[ ".dst", "file", "format", "extension", "API", "AutoCAD Sheet Set" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST - ไฟล์ชุดแผ่นงาน AutoCAD",
  "description" :"เรียนรู้เกี่ยวกับไฟล์ .dst และ API ที่สามารถสร้างและเปิดไฟล์ DST",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## ไฟล์ DST คืออะไร??

ไฟล์ DST เป็นไฟล์ AutoCAD ที่มีการเชื่อมโยงและข้อมูลสำหรับการกำหนดชุดแผ่นงาน สิ่งเหล่านี้ถูกจัดเก็บไว้ในโฟลเดอร์จัดเก็บชุดแผ่นงานเริ่มต้น ชุดแผ่นงาน AutoCAD ไฟล์ DST ไม่มีเค้าโครงการวาดภาพจริง แต่อ้างอิงจากไฟล์ [DWG](/th/cad/dwg/) และ [DWT](/th/cad/dwt/) ที่เลือกซึ่งเชื่อมโยงกับชุดแผ่นงานเหล่านี้ ในสภาพแวดล้อมเครือข่าย สมาชิกในทีมทุกคนควรมีสิทธิ์เข้าถึงเครือข่ายไปยังไฟล์ที่เกี่ยวข้องเหล่านี้ ไฟล์ DST จะถูกบันทึกลงดิสก์ในรูปแบบไฟล์ [XML](/th/web/xml/)

## รูปแบบไฟล์ DST - ข้อมูลเพิ่มเติม

ไฟล์ DST ถูกสร้างขึ้นด้วยเครื่องมือ AutoDesk Sheet Set Manager (SSM) เมื่อมีคนในทีมเข้าถึงไฟล์ ไฟล์ DST จะเปิดขึ้นชั่วครู่แล้วจัดเก็บกลับด้วยข้อมูลที่อัปเดต การเข้าถึงไฟล์ DST เดียวกันพร้อมกันได้รับการจัดการโดยเครื่องมือ SSM ที่แสดงไอคอนแม่กุญแจเมื่อมีการเข้าถึงไฟล์

สถานะแผ่นงานสามารถอยู่ในสถานะใดก็ได้ต่อไปนี้ ณ เวลาใดเวลาหนึ่ง

* แผ่นสามารถแก้ไขได้
* แผ่นถูกล็อค
* แผ่นงานหายไปหรือพบในตำแหน่งโฟลเดอร์ที่ไม่คาดคิด

## อ้างอิง

* [เกี่ยวกับการใช้ชุดแผ่นงาน DST](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-577D8EA0-85F2-4829-B4F9-8CAD6F7AAACC)
* [เรียนรู้เกี่ยวกับชุดแผ่นงาน](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-34D889BC-19AD-4CD1-ADB1-F359D9B515FB)
* [ชุดแผ่นงาน Mastering AutoCAD](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)

