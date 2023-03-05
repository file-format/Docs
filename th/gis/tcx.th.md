{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ TCX- ไฟล์ XML ของศูนย์ฝึกอบรม",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ TCX และ API ที่สามารถสร้างและเปิดไฟล์ TCX",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## ไฟล์ TCX คืออะไร??

ไฟล์ TCX (Training Center XML) เป็นรูปแบบการแลกเปลี่ยนข้อมูลที่ใช้ในการแบ่งปันข้อมูลระหว่างอุปกรณ์ออกกำลังกาย เปิดตัวในปี 2008 ด้วยผลิตภัณฑ์ Training Center ของ Garmin ข้อมูลการออกกำลังกาย เช่น อัตราการเต้นของหัวใจ จังหวะการวิ่ง จังหวะจักรยาน แคลอรี่ และเวลารอบจะถูกจัดเก็บในรูปแบบ [XML](/th/web/xml/) ภายในไฟล์ TCX นอกจากนี้ ข้อมูลสรุปเกี่ยวกับแทร็กออกกำลังกายยังรวมอยู่ในไฟล์ TCX ไฟล์ TCX คล้ายกับไฟล์ [FIT](/th/gis/fit/) ที่สร้างขึ้นด้วยอุปกรณ์สวมใส่กีฬา Garmin

## รูปแบบไฟล์ TCX - ข้อมูลเพิ่มเติม

ไฟล์ TCX จะถูกบันทึกลงดิสก์เป็นไฟล์ XML โดยบันทึกแต่ละรายการเป็นกิจกรรม กิจกรรมประกอบด้วยข้อมูลทั้งหมดของการออกกำลังกาย เช่น เวลา เวลารอบ Id อัตราการเต้นของหัวใจ ความหนัก จังหวะ และข้อมูลแทร็กที่มีคู่ของตำแหน่งพร้อมกับการประทับเวลาสำหรับตำแหน่งละติจูดที่คล้ายกับ [GPX](/th/gis/gpx/) ไฟล์

### เวอร์ชันรูปแบบไฟล์ TCX

รูปแบบนี้มีสองเวอร์ชันที่มี XML schema ของตนเองซึ่งโฮสต์โดย Garmin ต่อไปนี้เป็นบางส่วน:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## โปรโตคอลข้อมูล TCX

รูปแบบ TCX XML เวอร์ชันรวดเร็วพร้อมใช้งานบน Github ในชื่อ [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol)

## อ้างอิง ##

* [ศูนย์ฝึกอบรม XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [โปรแกรมดู TCX](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

