{
  "date" : "2021-08-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3ดีเอ็ม",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ 3DM และ API ที่สามารถเปิดและสร้างไฟล์ 3DM",
  "linktitle" : "3DM",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-08-13"
}

## ไฟล์ 3DM คืออะไร?

ไฟล์ที่มีนามสกุล .3dm เป็นรูปแบบไฟล์โอเพ่นซอร์สที่ใช้สำหรับซอฟต์แวร์กราฟิก 3 มิติ ประกอบด้วยโมเดล 3 มิติพร้อมกับองค์ประกอบที่ขึ้นต่อกัน เช่น พื้นผิว จุด และข้อมูลเส้นโค้ง รูปแบบไฟล์ 3DM ได้รับการพัฒนาโดยความคิดริเริ่มของ [openNURBS](https://github.com/mcneel/opennurbs) สำหรับการถ่ายโอนรูปทรงเรขาคณิต 3 มิติระหว่างแอปพลิเคชันอย่างแม่นยำ ไฟล์ 3DM สามารถเปิดและแปลงด้วยแอปพลิเคชันเช่น Rhinoceros, SAP VEViewer, Moment of Inspiration และ Right Hemisphere Deep View

## รูปแบบไฟล์ 3DM

[openNURBS](https://github.com/mcneel/opennurbs) ซึ่งเป็นชุดเครื่องมือโอเพนซอร์สประกอบด้วยข้อกำหนดรูปแบบไฟล์ 3DM เอกสารประกอบ ไลบรารีซอร์สโค้ด C++ และแอสเซมบลี .NET 2.0 เพื่ออ่านและเขียนรูปแบบไฟล์

### ไฟล์ตัวอย่าง 3DM

ไฟล์ 3DM ตัวอย่างบางส่วนสามารถดาวน์โหลดได้จากส่วน openNURBS [examples](https://github.com/mcneel/opennurbs/tree/7.x/example_files) สามารถโหลดและแสดงผลโดยใช้ชุดเครื่องมือ openNURBS

## จะอ่านหรือเขียนไฟล์ 3DM ได้อย่างไร?

ไลบรารี [openNURBS](https://github.com/mcneel/opennurbs) ช่วยให้ทุกคนสามารถอ่านและเขียนรูปแบบไฟล์ 3DM ได้โดยไม่ต้องใช้ Rhino มีซอร์สโค้ด C++ สำหรับไลบรารีที่จะอ่านและเขียนโมเดล 3 มิติโดยใช้รูปแบบไฟล์ openNURBS ชุดเครื่องมือนี้ยังมีเครื่องมือประเมิน NURBS และเครื่องมือจัดการมุมมองทางเรขาคณิตและมุมมอง 3 มิติเบื้องต้น รวมถึงซอร์สโค้ดสำหรับโปรแกรมตัวอย่างต่างๆ ฟอรัมสนับสนุน [Rhinoceros](https://discourse.mcneel.com/c/opennurbs/6) คือแหล่งรวมเนื้อหาและการสนทนามากมายเพื่อแชร์ปัญหาที่ชุมชน 3DM เผชิญและรับแนวทางแก้ไข

## อ้างอิง ##

* [แรด](https://www.rhino3d.com/download/openNURBS)
* [แรด - วิกิพีเดีย](https://en.wikipedia.org/wiki/Rhinoceros_3D)
* [openNURBS บน GitHub](https://github.com/mcneel/opennurbs)

