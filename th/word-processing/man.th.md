{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - คู่มือ Unix",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ FODT และ API ที่สามารถสร้างและเปิดไฟล์ MAN",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## ไฟล์ MAN คืออะไร??

ไฟล์ที่มีนามสกุล .man ย่อมาจาก man page ซึ่งเป็นคู่มือผู้ใช้การเขียนโปรแกรม Unix ในรูปแบบเอกสารซอฟต์แวร์ มันถูกใช้งานโดยยูทิลิตี `Man` ซึ่งรวมอยู่ใน Unix ซึ่งใช้เพื่อดูเอกสารประกอบ เอกสารประกอบของซอฟต์แวร์ประกอบด้วยข้อมูลในส่วนและหน้าที่สามารถเรียกค้นได้โดยใช้ยูทิลิตี้ Man จากเทอร์มินัลคำสั่งโดยการออกคำสั่ง พร้อมใช้งานในคอมพิวเตอร์ในรูปแบบสำเนาของเอกสาร ไม่จำเป็นต้องมีสำเนาที่พิมพ์หรือการเชื่อมต่ออินเทอร์เน็ตเพื่อเข้าถึง

## รูปแบบไฟล์ Unix Manual Man - ข้อมูลเพิ่มเติม

หน้าคนถูกจัดเก็บในรูปแบบข้อความธรรมดาและสามารถสร้างและเปิดในโปรแกรมแก้ไขข้อความเพื่อดูหรือแก้ไข ใน UNIX ข้อมูลจาก Man page จะถูกเรียกใช้โดยการออกคำสั่งจากเทอร์มินัลที่มีการอ้างอิงถึงส่วนและหมายเลขหน้าจากคู่มือ

### ส่วนและหน้า

Unix man เป็นคู่มือของระบบที่อาร์กิวเมนต์แต่ละหน้าของคำสั่งอ้างถึงชื่อของโปรแกรม ยูทิลิตี้ หรือฟังก์ชัน คำสั่ง ถ้ามีข้อมูลส่วน จะค้นหาหน้าในส่วนเฉพาะนั้น อย่างไรก็ตาม การทำงานเริ่มต้นคือการค้นหาหน้าในทุกส่วนและแสดงหน้าแรก โดยไม่คำนึงว่าหน้านั้นจะอยู่ในหลายส่วนหรือไม่

### หมายเลขมาตรา

ต่อไปนี้เป็นข้อมูลเกี่ยวกับหมายเลขส่วนของคู่มือตามด้วยประเภทของหน้าที่บรรจุอยู่

|หมายเลขมาตรา|ประเภทของหน้า|
---|---|
|1|โปรแกรมปฏิบัติการหรือคำสั่งเชลล์|
|2|การเรียกของระบบ (ฟังก์ชันที่มีให้โดยเคอร์เนล)|
|3|การเรียกใช้ไลบรารี (ฟังก์ชันภายในไลบรารีของโปรแกรม)|
|4|ไฟล์พิเศษ (มักพบใน /dev)|
|5|รูปแบบไฟล์และข้อตกลง เช่น /etc/passwd|
|6|เกม|
|7|เบ็ดเตล็ด (รวมถึงมาโครแพ็คเกจและแบบแผน) เช่น man(7), groff(7)|
|8|คำสั่งการดูแลระบบ (ปกติสำหรับรูทเท่านั้น)|
|9|กิจวัตรเคอร์เนล [ไม่ใช่มาตรฐาน]|

## ตัวอย่าง - จะอ่านหน้า MAN ได้อย่างไร

ต่อไปนี้เป็นตัวอย่างวิธีการดึงข้อมูลของคำสั่ง MkDir โดยใช้คำสั่ง Man

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## อ้างอิง

* [ข้อกำหนดทางเทคนิคของ OpenDocument - โดย Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_ specification)
* [man(1) — หน้าคู่มือ Linux](https://man7.org/linux/man-pages/man1/man.1.html)

