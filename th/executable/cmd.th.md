{
  "date" : "2021-07-12",
  "keywords" :[ "ไฟล์ cmd", "ไฟล์ cmd คืออะไร", "ไฟล์", "ตัวอย่าง cmd", "นามสกุลไฟล์ cmd", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CMD และ API ที่สามารถสร้างและเปิดไฟล์ CMD",
  "title" :"CMD - รูปแบบไฟล์คำสั่ง Windows",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## ไฟล์ CMD คืออะไร??
ไฟล์ CMD ประกอบด้วยสคริปต์ที่มีคำสั่งหนึ่งหรือหลายคำสั่งในรูปแบบของข้อความธรรมดาที่เรียกใช้เพื่อดำเนินการงานต่างๆ ซึ่งคล้ายกับไฟล์ [BAT](/th/executable/bat/) ซึ่งโดยทั่วไปจะใช้ในการจัดเก็บชุดคำสั่งปฏิบัติการ ไฟล์ CMD ใช้กันอย่างแพร่หลายในระบบปฏิบัติการ Microsoft Windows ไฟล์เหล่านี้ถูกนำมาใช้ในเกือบ 90 ปี แต่ยังคงใช้ในระบบปฏิบัติการ Windows รุ่นล่าสุด โดยทั่วไปแล้วไฟล์เหล่านี้จะถูกเขียนขึ้นเพื่อดำเนินการมากกว่าหนึ่งคำสั่งในลำดับ

## รูปแบบไฟล์ CMD
CMD เป็นรูปแบบไฟล์ที่ใช้โดยโปรแกรมปฏิบัติการแบบ CP/M โดยทั่วไปเทียบได้กับ [COM](/th/executable/com/) ใน CP/M-80 และ [EXE](/th/executable/exe/) ใน DOS ไฟล์ CMD มีรหัสหรือข้อมูล 1 ถึง 8 กลุ่มและส่วนหัว 128 ไบต์ แต่ละกลุ่มมีขนาดไม่เกิน 1 mb ไฟล์ CMD ยังสามารถมีข้อมูลการย้ายตำแหน่งและ Resident System Extensions (RSXs) ในเวอร์ชันที่ใหม่กว่า CMD เป็นไฟล์ใหม่เมื่อเปรียบเทียบกับไฟล์ [BAT](/th/executable/bat/); ใช้สำหรับ MS-DOS ก่อนการเปิดตัว Windows ใน MS-DOS แม้ว่าคุณจะยังคงสามารถบันทึกไฟล์ที่มีนามสกุล .bat ได้ในปัจจุบัน แต่หลายคนใช้นามสกุล .cmd เพื่อบันทึกสคริปต์สั่งการของพวกเขา

### ข้อกำหนดรูปแบบ CMD

จุดเริ่มต้นของส่วนหัวประกอบด้วยรายการของกลุ่มที่มีอยู่ในไฟล์พร้อมกับประเภท แต่ละประเภทสามารถใช้ได้สูงสุดหนึ่งครั้ง ประเภทเหล่านี้คือ:

- รหัส
- ข้อมูล
- พิเศษ
- ซ้อนกัน
- ผู้ใช้ 1
- ผู้ใช้ 2
- ผู้ใช้ 3
- ผู้ใช้ 4
- รหัสที่ใช้ร่วมกัน

ในทำนองเดียวกันคำนำหน้ากลุ่มโปรแกรมใน DOS 256 ไบต์แรกของกลุ่มข้อมูลจะเป็นศูนย์ พวกเขาจะถูกเติมโดย CP/M-86 โดยมีหน้าเป็นศูนย์ หากไม่มีกลุ่มข้อมูล ระบบจะใช้ 256 ไบต์แรกของกลุ่มรหัสแทน
## ตัวอย่างไฟล์ CMD
ต่อไปนี้เป็นตัวอย่างของสคริปต์ CMD เพื่อแสดงข้อมูลระบบ
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## อ้างอิง

* [วิธีเขียนสคริปต์ CMD](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [ไฟล์ CMD (CP/M) - โดย Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

