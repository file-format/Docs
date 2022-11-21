{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - ไฟล์ติดต่อเสมือน",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ VCF และ API ที่สามารถสร้างและเปิดไฟล์ VCF",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ VCF คืออะไร??

VCF (Virtual Card Format) หรือ vCard เป็นรูปแบบไฟล์ดิจิทัลสำหรับจัดเก็บข้อมูลผู้ติดต่อ รูปแบบนี้ใช้กันอย่างแพร่หลายสำหรับการแลกเปลี่ยนข้อมูลระหว่างแอปพลิเคชันแลกเปลี่ยนข้อมูลที่เป็นที่นิยม ระบบปฏิบัติการส่วนใหญ่ เช่น Windows และ MacOS มาพร้อมกับแอปพลิเคชันเริ่มต้นสำหรับสร้างและเปิดไฟล์เหล่านี้ ไฟล์ VCF ไฟล์เดียวสามารถมีข้อมูลผู้ติดต่อหนึ่งหรือหลายผู้ติดต่อ ไฟล์ VCF มักประกอบด้วยข้อมูล เช่น ชื่อผู้ติดต่อ ที่อยู่ หมายเลขโทรศัพท์ อีเมล วันเกิด รูปถ่ายและเสียง นอกเหนือไปจากฟิลด์อื่นๆ อีกจำนวนหนึ่ง ได้รับการสนับสนุนโดยไคลเอนต์อีเมลและบริการ ข้อมูลจะไม่สูญหายระหว่างการถ่ายโอนผู้ติดต่อโดยใช้รูปแบบ vCard ประเภทสื่อสำหรับรูปแบบไฟล์ VCF คือ text/vcard

## รูปแบบไฟล์ VCF

ไฟล์ VCF เป็นข้อความโดยธรรมชาติและมนุษย์สามารถอ่านได้ สามารถเปิดได้ในโปรแกรมแก้ไขข้อความ เช่น Notepad บน Microsoft Windows และ TextEdit บน MacOS อย่างไรก็ตาม หากมีรูปภาพในไฟล์ จะไม่แสดงในโปรแกรมแก้ไขข้อความ

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) ให้การสนับสนุน การเปิดไฟล์ VCF และแปลงเป็นรูปแบบอื่นๆ เช่น รูปแบบ [MSG](/th/email/msg/) ยอดนิยม รูปแบบไฟล์ VCF ปรับปรุงตามเวลาตั้งแต่เวอร์ชัน 2.1 ถึง 4.0 โดยเพิ่มข้อมูลโดยละเอียดให้กับรูปแบบไฟล์ รูปแบบนี้ยังใช้เพื่อส่งออกรายชื่อติดต่อทางโทรศัพท์และนำเข้าในอุปกรณ์อื่นในภายหลัง

{{< figure src="../VCF.png" alt="รูปแบบไฟล์ VCF" >}}

### ตัวอย่าง VCF 2.1

ต่อไปนี้เป็นตัวอย่างของเวอร์ชัน 2.1

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### ตัวอย่าง VCF 3.0

ต่อไปนี้เป็นตัวอย่างของเวอร์ชัน 3.0

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### ตัวอย่าง VCF 4.0

ต่อไปนี้เป็นตัวอย่างของเวอร์ชัน 4.0

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## อ้างอิง

* [VCF - โดย Wikipedia](https://en.wikipedia.org/wiki/VCard)

