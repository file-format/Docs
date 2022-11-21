{
  "date" : "2021-06-09",
  "keywords" :[ "คิว", "ไฟล์", "นามสกุล", "รูปแบบ", "ไฟล์คิวคืออะไร", "เพลง", "รูปแบบไฟล์คิว", "ข้อกำหนดรูปแบบไฟล์คิว", "คิวชีท", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CUE และ API ที่สามารถสร้าง แปลง และเปิดไฟล์ CUE",
  "title" :"CUE - ไฟล์คิวชีท",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## ไฟล์ CUE คืออะไร??

ไฟล์ที่มีนามสกุล .cue หรือที่เรียกว่าไฟล์แผ่นคิว เป็นไฟล์ข้อมูลเมตาที่มีข้อมูลเกี่ยวกับเค้าโครงของแทร็กในซีดีหรือดีวีดี สิ่งเหล่านี้ได้รับการสนับสนุนโดยเครื่องเล่นมีเดียและแอปพลิเคชันเขียนแผ่นออปติคัล ข้อมูลเสียงหลักที่จัดเก็บไว้ในซีดีจะถูกอ้างอิงโดยไฟล์คิว พร้อมด้วยข้อมูลจำเพาะของความยาวแทร็ก ชื่อดิสก์ และผู้แสดง ดังนั้น หากไฟล์เสียงไฟล์เดียวมีหลายแทร็ก สามารถใช้ไฟล์คิวเพื่อแบ่งเสียงออกเป็นหลายไฟล์หรืออ้างอิงแทร็กต่างๆ ได้

## รูปแบบไฟล์ CUE

ไฟล์ CUE หรือคิวชีตถูกจัดเก็บไว้ในรูปแบบข้อความธรรมดาที่มนุษย์สามารถอ่านได้ ข้อมูลในไฟล์คิวเป็นคำสั่งที่มีพารามิเตอร์ตั้งแต่หนึ่งตัวขึ้นไป คำสั่งเหล่านี้ใช้กับทั้งไฟล์หรือกับแต่ละแทร็ก ขึ้นอยู่กับคำสั่งเฉพาะและบริบท คู่มือผู้ใช้ CDRWIN อธิบายข้อกำหนดสำหรับไวยากรณ์และซีแมนทิกส์ของคิวชีต

## คำสั่งสำคัญของ CUE Sheet

|คำสั่ง|คำอธิบาย|
---|---|
|ไฟล์| หมายถึงไฟล์ที่มีข้อมูลและรูปแบบ เช่น [MP3](/th/audio/mp3/), [WAV](/th/audio/wav/) หรืออิมเมจดิสก์ไบนารีธรรมดา)|
|ติดตาม| กำหนดข้อมูลบริบทของแทร็ก เช่น หมายเลขและประเภทหรือโหมด|
|ดัชนี| แสดงตำแหน่งเป็นดัชนีภายในไฟล์ รูปแบบคือ mm:ss:ff (นาที-วินาที-เฟรม)|
|PREGAP และ POSTGAP|สิ่งนี้บ่งชี้ถึงช่องว่างก่อนหรือหลังช่องว่างของแทร็ก ซึ่งไม่ได้จัดเก็บไว้ในไฟล์ข้อมูลใดๆ ความยาวระบุในรูปแบบนาที-วินาที-เฟรมเดียวกับสำหรับ INDEX|

### ตัวอย่างแผ่น CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## อ้างอิง

* [ไฟล์ .cda - โดย Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

