{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ VPK - รูปแบบไฟล์แพ็คเกจแอปพลิเคชัน PlayStation Vita",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ VPK และ API ที่สามารถสร้างและเปิดไฟล์ VPK",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## ไฟล์ VPK คืออะไร??

ไฟล์ที่มีนามสกุล .vpk คือไฟล์แพ็กเกจไฟล์เก็บถาวรแบบบีบอัดที่ใช้ในการติดตั้งแอปของบุคคลที่สามบนคอนโซลเกม Sony PlayStation Vita ไฟล์เหล่านี้สามารถติดตั้งได้เฉพาะในการเจลเบรค Vita PlayStation โดย HENkaku ซึ่งทำให้ PS Vita และ PSTV ใช้เนื้อหาที่ผู้ใช้สร้างขึ้นเอง ไฟล์เก็บถาวร VPK มีเนื้อหาทั้งหมดที่ประกอบกันเป็นเกม รวมถึงรูปภาพ เช่น ไฟล์ [PNG](/th/image/png/) ไฟล์การตั้งค่า เช่น [.bin](/th/disc-and-media/bin/) และ การกำหนดค่าใดๆ ในรูปแบบไฟล์ [XML](/th/web/xml/)

## รูปแบบไฟล์ VPK

ไฟล์ VPK ถูกบันทึกลงดิสก์เป็นไฟล์เก็บถาวรมาตรฐาน [ZIP](/th/compression/zip/) สิ่งเหล่านี้อาจมีหลายโฟลเดอร์และไฟล์ที่เกี่ยวข้องอื่นๆ สำหรับแอปของบุคคลที่สามที่จะติดตั้งบน Vita Gaming Console หากต้องการดูเนื้อหาของไฟล์แพ็คเกจ VPK ให้เปลี่ยนชื่อนามสกุลจาก .vpu เป็น .zip และแยกเนื้อหาโดยใช้ยูทิลิตี้คลายการบีบอัดมาตรฐาน เช่น WinZip หรือ WinRAR

Valvesoftware มีข้อมูลโดยละเอียดเกี่ยวกับ [รูปแบบไฟล์ VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format) ที่สามารถอ้างอิงได้จากมุมมองของผู้พัฒนา

## จะติดตั้งไฟล์ VPK ได้อย่างไร?

ไฟล์ VPK สามารถติดตั้งได้จากยูทิลิตี้บรรทัดคำสั่ง VPK.exe บนระบบปฏิบัติการ Windows สามารถทิ้งไฟล์บนไฟล์ vpk.exe ซึ่งส่งคืน \*.vpk ที่มีไฟล์แพ็คเกจทั้งหมด หรือสามารถใช้ command line tool ได้ดังนี้

### สร้าง VPK และเพิ่มไฟล์

```
vpk <dirname>
```

### แยกไฟล์ VPK

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## โปรแกรมดู VPK

* [โปรแกรมดู VRF VPK](https://github.com/SteamDatabase/ValveResourceFormat)

## อ้างอิง

* [รูปแบบไฟล์ VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [ไฟล์ VPK](https://developer.valvesoftware.com/wiki/VPK)

