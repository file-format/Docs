{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "นามสกุล", "ไฟล์", "รูปแบบ", "ระบบ", "ไดรเวอร์", "ไดรเวอร์อุปกรณ์ Windows", "โปรแกรม", "คอมพิวเตอร์", "แอปพลิเคชัน" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - ไดรเวอร์อุปกรณ์ Windows",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ DRV และ API ที่สามารถสร้างและเปิดไฟล์ DRV",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## ไฟล์ DRV คืออะไร?? ##

ไฟล์ที่มีนามสกุล .drv เป็นของ Windows Device Driver ระบบปฏิบัติการ Windows ใช้ไฟล์เหล่านี้เพื่อเชื่อมต่ออุปกรณ์ฮาร์ดภายในและภายนอก ไฟล์ DRV ประกอบด้วยคำแนะนำและพารามิเตอร์สำหรับการเชื่อมโยงอุปกรณ์และระบบปฏิบัติการเข้าด้วยกัน ไฟล์เหล่านี้ช่วยในการติดตั้งไดรเวอร์อุปกรณ์เพื่อให้ทำงานได้อย่างถูกต้องกับ Windows นอกจากนี้ อุปกรณ์ที่เชื่อมโยงกับเมนบอร์ดของพีซีผ่านบัสหรือสายเคเบิลจำเป็นต้องมีไฟล์ DRV


## รูปแบบไฟล์ DRV ##

ไฟล์ DRV มักจะถูกบรรจุเป็นไดนามิกไลบรารี (ไฟล์ [DDL](/th/system/dll/)) หรือไฟล์ [EXE](/th/executable/exe/) ไฟล์เหล่านี้สามารถรองรับได้ในทุกแพลตฟอร์มระบบ เช่น สมาร์ทโฟน และไม่มีการรับประกันว่าแต่ละแพลตฟอร์มจะรองรับไฟล์เหล่านี้อย่างเหมาะสม อย่างไรก็ตาม อุปกรณ์ทั่วไปบางส่วนที่ใช้นามสกุลไฟล์ .drv คือ:

* การ์ดเสียง
* การ์ดจอ
* เครื่องพิมพ์
* อุปกรณ์จัดเก็บข้อมูล
* อะแดปเตอร์เครือข่าย
* อุปกรณ์ฮาร์ดแวร์คอมพิวเตอร์

ไม่แนะนำให้เปิดไฟล์ DRV ที่ส่งทางอีเมล เนื่องจากรูปแบบไฟล์นี้มีไวรัสและโปรแกรมที่เป็นอันตรายอื่นๆ ตรวจสอบให้แน่ใจว่าได้ทำการสแกนอย่างละเอียดก่อนที่จะเปิดไฟล์ DRV ที่ไม่รู้จัก


## ตัวอย่าง DRV ##

```
// Include necessary files...
#include <font.defs>
#include <media.defs>
#include <hp.h>
#include <epson.h>
#include <label.h>

// Localizations are provided for all of the base languages supported by
// CUPS...
#po ar ""
#po ca ""
#po de ""
#po el ""
#po es ""
#po fr ""
#po no ""
#po ru ""
#po sk ""
#po sv ""
#po th ""
#po tr ""
#po uk ""

// MediaSize sizes used by label drivers...
#media "w90h18/1.25x0.25\"" 90 18
#media "w90h162/1.25x2.25\"" 90 162
#media "w108h18/1.50x0.25\"" 108 18
#media "w108h36/1.50x0.50\"" 108 36
#media "w108h72/1.50x1.00\"" 108 72
#media "w108h144/1.50x2.00\"" 108 144
#media "w144h26/2.00x0.37\"" 144 26
#media "w576h360/8.00x5.00\"" 576 360
#media "w576h432/8.00x6.00\"" 576 432
#media "w576h468/8.00x6.50\"" 576 468

// Common stuff for all drivers...
Attribute "cupsVersion" "" "2.2"
Attribute "FileSystem" "" "False"
Attribute "LandscapeOrientation" "" "Plus90"
Attribute "TTRasterizer" "" "Type42"

Font *

Version "2.1"

// Dymo Label Printer
{
  Manufacturer "Dymo"
  ModelName "Label Printer"
  Attribute NickName "" "Dymo Label Printer"
  PCFileName "dymo.ppd"
  DriverType label
  ModelNumber $DYMO_3x0
  Throughput 8
  ManualCopies Yes
  ColorDevice No

  HWMargins 2 14.9 2 14.9

  *MediaSize w81h252
  MediaSize w101h252
  MediaSize w54h144
  MediaSize w167h288
  MediaSize w162h540
  MediaSize w162h504
  MediaSize w41h248
  MediaSize w41h144
  MediaSize w153h198

  Resolution k 1 0 0 0 136dpi
  Resolution k 1 0 0 0 203dpi
  *Resolution k 1 0 0 0 300dpi

  Darkness 0 Light
  Darkness 1 Medium
  *Darkness 2 Normal
  Darkness 3 Dark
}

```

