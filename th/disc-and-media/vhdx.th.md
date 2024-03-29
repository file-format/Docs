{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ VHDX และ API ที่สามารถสร้างและเปิดไฟล์ VHDX",
  "title" :"รูปแบบไฟล์ VHDX - ไฟล์ VHDX คืออะไร",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## ไฟล์ VHDX คืออะไร??

ไฟล์ VHDX เป็นไฟล์ภาพดิสก์ในรูปแบบไฟล์ Virtual Hard Disk v2 ประกอบด้วยระบบปฏิบัติการทั้งหมดที่สามารถโหลดและใช้งานเหมือนเครื่องทั่วไปสำหรับการทดสอบซอฟต์แวร์หรือรันซอฟต์แวร์ที่ต้องใช้ระบบปฏิบัติการเฉพาะ VHDX แม้จะเป็นอิมเมจของดิสก์แบบเต็ม แต่ก็ถูกจัดเก็บไว้ในไฟล์เดียว ซอฟต์แวร์เครื่องเสมือน เช่น Parallels Desktop, Windows Virtual Machine และ Virtual Box สามารถโหลดและเปิดภาพดิสก์ได้

ไฟล์ VHDX สามารถแปลงเป็น [VHD](/th/disc-and-media/vhd/) ด้วย Hyper-V Manager หรือเป็น [VDI](/th/disc-and-media/vdi/) ด้วย VirtualBox

## รูปแบบไฟล์ VHDX - ข้อมูลเพิ่มเติม

รายละเอียดรูปแบบไฟล์ VHDX ได้รับการบันทึกไว้อย่างสมบูรณ์และพร้อมใช้งานทางออนไลน์ในชื่อ ) บนเอกสาร Microsoft เป็นส่วนเสริมของรูปแบบ VHD และมีความสามารถที่เพิ่มขึ้น รูปแบบไฟล์ VHDX มีคุณสมบัติเพิ่มเติมที่มีอยู่ในชั้นของไฟล์ฮาร์ดดิสก์เสมือนและฮาร์ดดิสก์เสมือน ได้รับการปรับให้เหมาะสมยิ่งขึ้นและให้ผลลัพธ์ที่ดีกว่าสำหรับการกำหนดค่าและความสามารถของฮาร์ดแวร์สตอเรจ ไฟล์ VHDX สามารถเปิดได้

### รองรับฮาร์ดดิสก์เสมือนใน VHDX

รองรับฮาร์ดดิสก์เสมือนสามประเภท

1. **Fixed Virtual Hard Disk** - ฮาร์ดดิสก์เสมือนที่มีการจัดสรรขนาดข้อมูลคงที่ ขนาดของฮาร์ดดิสก์เสมือนจะไม่เปลี่ยนแปลงเมื่อมีการเพิ่มหรือลบข้อมูล

1. **Dynamic Virtual Hard Disk** - ฮาร์ดดิสก์เสมือนที่มีขนาดไดนามิกดิสก์ ขนาดของมันมีขนาดใหญ่เท่ากับข้อมูลจริงที่เขียนและข้อมูลเมตา ขนาดไฟล์จะเพิ่มขึ้นแบบไดนามิกเมื่อมีการเพิ่มหรือลบข้อมูลออกจากไฟล์

1. **ความแตกต่างของฮาร์ดดิสก์เสมือน** - แสดงถึงปัจจุบันของฮาร์ดดิสก์เสมือนเป็นชุดของบล็อกที่แก้ไขเมื่อเปรียบเทียบกับไฟล์ฮาร์ดดิสก์เสมือนหลัก

## อ้างอิง

* [ข้อกำหนดรูปแบบไฟล์ VHDX](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - โดย Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))

