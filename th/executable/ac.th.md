{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "เรียนรู้เกี่ยวกับรูปแบบไฟล์ AC และ API ที่สามารถสร้างและเปิดไฟล์ ACCDB",
  "title" : "รูปแบบไฟล์ AC - ไฟล์สคริปต์ Autoconf",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-th",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## ไฟล์ AC คืออะไร

ไฟล์ AC เป็นไฟล์สคริปต์ Autoconf **Autoconf** เป็นแพ็คเกจขยายได้ของมาโคร M4 ที่สร้างเชลล์สคริปต์เพื่อกำหนดค่าแพ็คเกจซอร์สโค้ดซอฟต์แวร์โดยอัตโนมัติ สคริปต์เหล่านี้สามารถปรับแพ็คเกจให้เข้ากับระบบที่คล้ายกับ UNIX หลายประเภท โดยที่ผู้ใช้ไม่ต้องดำเนินการเอง Autoconf จะสร้างสคริปต์การกำหนดค่าสำหรับแพ็คเกจจากไฟล์เทมเพลตที่แสดงรายการคุณสมบัติของระบบปฏิบัติการที่แพ็คเกจสามารถใช้ได้ ในรูปแบบของการเรียกแมโคร M4

Producing configuration scripts using Autoconf requires GNU M4. คุณควรติดตั้ง GNU M4 (อย่างน้อยเวอร์ชัน 1.4.6 แม้ว่าแนะนำให้ใช้ 1.4.13 หรือใหม่กว่าก็ตาม) ก่อนที่จะกำหนดค่า Autoconf เพื่อให้สคริปต์กำหนดค่าของ Autoconf สามารถค้นหาได้ สคริปต์การกำหนดค่าที่สร้างโดย Autoconf นั้นมีอยู่ในตัวเอง ดังนั้นผู้ใช้จึงไม่จำเป็นต้องมี Autoconf (หรือ GNU M4)

## เปิดไฟล์ AC ได้อย่างไร

AC ย่อมาจากการกำหนดค่าอัตโนมัติ เป็นสคริปต์ที่สร้างโดย GNU Autoconf ซึ่งช่วยให้ซอร์สโค้ดซอฟต์แวร์สามารถปรับให้เข้ากับระบบที่คล้ายกับ Posix ต่างๆ โดยการทดสอบคุณสมบัติที่จำเป็นในแพ็คเกจ สคริปต์นี้เรียกว่าไฟล์ AC

## ส่วนประกอบ Autotools ที่สำคัญ

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools คือชุดของแพ็คเกจที่เกี่ยวข้อง ซึ่งเมื่อใช้ร่วมกัน จะช่วยลดความยุ่งยากในการสร้างซอฟต์แวร์พกพาได้มาก เครื่องมือเหล่านี้ พร้อมด้วยไฟล์อินพุตที่มาจากอัพสตรีมที่ค่อนข้างเรียบง่าย ถูกนำมาใช้เพื่อสร้างระบบบิลด์สำหรับแพ็คเกจ

**ภาพรวมเบื้องต้นว่าส่วนประกอบหลักของเครื่องมืออัตโนมัติประกอบเข้าด้วยกันได้อย่างไร**

!{{ไฮเปอร์ลิงก์1}}

ในการตั้งค่าง่ายๆ:

- โปรแกรม `autoconf` จะสร้างสคริปต์กำหนดค่าจาก `configure.in` หรือ `configure.ac`
- โปรแกรม `automake` สร้าง Makefile.in จาก Makefile.am
- เรียกใช้สคริปต์ 'กำหนดค่า' เพื่อสร้างไฟล์ Makefile หนึ่งไฟล์ขึ้นไปจากไฟล์ Makefile.in
- โปรแกรม `make` ใช้ Makefile เพื่อคอมไพล์โปรแกรม

## อ้างอิง
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [พื้นฐานของ Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



