{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ ADM - รูปแบบไฟล์เทมเพลตการดูแลระบบ",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ ADM และวิธีเปิดไฟล์ ADM",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## ไฟล์ ADM คืออะไร??

ไฟล์ ADM เป็นไฟล์เทมเพลตที่ใช้โดยซอฟต์แวร์ Microsoft Group Policies เพื่อระบุตำแหน่งของการตั้งค่านโยบายตามรีจิสทรีในไฟล์รีจิสทรี ผู้ดูแลระบบใช้เพื่อกำหนดนโยบายในการจัดการกลุ่มคอมพิวเตอร์ที่เป็นส่วนหนึ่งของกลุ่ม ข้อมูลนี้กลายเป็นส่วนหนึ่งของ Group Policy Objects (GPO) ที่สร้างขึ้นสำหรับการจัดการกลุ่ม

คุณสามารถเปิดไฟล์ ADM ได้โดยใช้ Microsoft Group Policy Object Editor

## รูปแบบไฟล์ ADM - ข้อมูลเพิ่มเติม

ไฟล์ ADM จะถูกจัดเก็บเป็นไฟล์ข้อความในรูปแบบยูนิโค้ด สิ่งเหล่านี้ใช้เพื่ออธิบายตำแหน่งของการตั้งค่านโยบายตามรีจิสทรีในรีจิสทรี Windows Vista และ Windows 7 เป็นหลัก

ไฟล์ ADM ไม่ได้รับการสนับสนุนอีกต่อไป และถูกแทนที่ด้วยไฟล์ [ADMX](/th/system/admx/) GPA จะละเว้นไฟล์ ADM เริ่มต้นต่อไปนี้บนคอมพิวเตอร์ที่ใช้ Microsoft Windows Vista Service Pack 1 หรือใหม่กว่า

* system.adm
* inetres.adm
* ยืนยันadm
* wmplayer.adm
* wuau.adm

## อ้างอิง

* [ไฟล์เทมเพลตการดูแลระบบ - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - การจัดการไฟล์เทมเพลตการดูแลระบบ](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

