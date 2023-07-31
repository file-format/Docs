{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ SY_ - ไฟล์ SYS ที่บีบอัด",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ SY_ และ API ที่สามารถสร้างและเปิดไฟล์ SY_",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## ไฟล์ SY_ คืออะไร??

ไฟล์ SY_ เป็นไฟล์ .sys ที่ถูกบีบอัดซึ่งใช้โดยโปรแกรมติดตั้งซอฟต์แวร์เพื่อลดขนาดของไฟล์การติดตั้งที่บรรจุอยู่ภายในโปรแกรมติดตั้ง ซึ่งจะลดขนาดโดยรวมของตัวติดตั้ง ไฟล์ SY_ สามารถขยายได้โดยใช้ยูทิลิตีบรรทัดคำสั่ง Microsoft Expand ที่ขยายไฟล์บีบอัดตั้งแต่หนึ่งไฟล์ขึ้นไป

## รูปแบบไฟล์ SY_ - ข้อมูลเพิ่มเติม

ไฟล์ SY_ ถูกบันทึกลงในดิสก์เป็นไฟล์ไบนารีที่บีบอัด อย่างไรก็ตาม รูปแบบไฟล์ภายในไม่เปิดเผยต่อสาธารณะ ยูทิลิตีบรรทัดคำสั่ง Microsoft Expand สามารถขยายไฟล์ SY_ โดยใช้หนึ่งในบรรทัดคำสั่งต่อไปนี้

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
เมื่อขยาย ไฟล์ SY_ จะถูกแปลงเป็นไฟล์ [SYS](https://docs.fileformat.com/system/sys/)

ไฟล์ SY_ คล้ายกับไฟล์ EX_ และ DL_

## อ้างอิง

* [StuffIt - โดย Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

