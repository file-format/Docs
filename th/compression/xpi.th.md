{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - ไฟล์แพ็คเกจตัวติดตั้งข้ามแพลตฟอร์ม",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ XPI และ API ที่สามารถสร้างและเปิดไฟล์ XPI",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## ไฟล์ XPI คืออะไร??

ไฟล์ XPI เป็นไฟล์เก็บถาวรการติดตั้งที่ถูกบีบอัดเพื่อลดขนาดของไฟล์ แอปพลิเคชัน Mozilla ใช้สำหรับติดตั้งปลั๊กอินและไฟล์เสริม ประกอบด้วยสคริปต์การติดตั้งหรือรายการที่รูทของไฟล์พร้อมกับไฟล์ข้อมูลจำนวนหนึ่ง ไฟล์ XPI อาจมีธีม ชุดเครื่องมือ หรือปลั๊กอิน Firefox ที่ผู้ใช้สามารถติดตั้งเพื่อเป็นส่วนหนึ่งของเบราว์เซอร์ Firefox, Thunderbird หรือ SeaMonkey

## รูปแบบไฟล์ XPI - ข้อมูลเพิ่มเติม

ไฟล์ XPI จะถูกบันทึกลงดิสก์เป็นไฟล์เก็บถาวร [ZIP](/th/compression/zip/) ที่รวมไฟล์หลายไฟล์ไว้ในไฟล์บีบอัดไฟล์เดียว ไฟล์ภายในไฟล์ XPI อาจรวมถึงไฟล์สคริปต์การติดตั้ง เช่น JS และไฟล์เว็บ เช่น [CSS](/th/web/css/), [HTML](/th/web/html/) และ [JSON](/th/web/json/ ). บางครั้ง อาจมีไฟล์รูปภาพ [PNG](/th/image/png/) ที่จะใช้เป็นไอคอนโดยโปรแกรมเสริม

### วิธีการดูเนื้อหาของไฟล์ XPI?

ไฟล์ XPI เป็นไฟล์เก็บถาวร ZIP ซึ่งเนื้อหาสามารถดูได้โดยใช้ขั้นตอนต่อไปนี้

* เปลี่ยนนามสกุลไฟล์จาก XPI เป็น ZIP
* แยกเนื้อหาของไฟล์โดยใช้ยูทิลิตี้คลายการบีบอัดมาตรฐาน เช่น WinZip (Windows, Mac), 7-Zip (Windows) หรือ Apple Archive Utility (Mac)

### ติดตั้งไฟล์ XPI บน Firefox Android

คนส่วนใหญ่อยากรู้ว่าไฟล์ XPI สามารถติดตั้งใน Firefox บนอุปกรณ์ Android ได้หรือไม่ บน Android คุณสามารถติดตั้งส่วนเสริมจากไฟล์ XPI ได้โดยค้นหาไฟล์และเปิดด้วย Firefox

## อ้างอิง

* [XPInstall - วิกิพีเดีย](https://en.wikipedia.org/wiki/XPInstall)
* [ฉันจะเปิดไฟล์นามสกุล XPI ได้อย่างไร](https://support.mozilla.org/en-US/questions/1009049)
