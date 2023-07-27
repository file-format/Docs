{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ TGZ - ไฟล์ Gzip Tar",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ TGZ และ API ที่สามารถสร้างและเปิดไฟล์ TGZ",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## ไฟล์ TGZ คืออะไร??

ไฟล์ที่มีนามสกุล .tgz คือไฟล์เก็บถาวร TAR ซึ่งประกอบด้วยไฟล์และโฟลเดอร์หลายไฟล์ ซึ่งได้รับการบีบอัดโดยใช้ซอฟต์แวร์บีบอัด Gnu Zip (gzip) ไฟล์ [TAR](/th/compression/tar/) มักจะรวมไฟล์หลายไฟล์เป็นไฟล์เดียวสำหรับการสำรองข้อมูลหรือแจกจ่ายทางอินเทอร์เน็ต เป็นไฟล์ที่ไม่บีบอัดจนกว่าจะบีบอัดโดยใช้ซอฟต์แวร์ gzip หลังจากนั้นจึงกลายเป็นไฟล์ TGZ ไฟล์ TGZ เป็นไฟล์บีบอัด ใช้พื้นที่บนดิสก์น้อย และสามารถโอนผ่านอินเทอร์เน็ตผ่านอีเมลได้อย่างง่ายดาย แอปพลิเคชั่นบางตัวที่สามารถเปิดไฟล์ TGZ ได้แก่ WinZip, Apple Archive Utility, 7-Zip และ WinRAR ไฟล์ TGZ ส่วนใหญ่จะใช้ในระบบ UNIX และ Linux

## รูปแบบไฟล์ TGZ

ไฟล์ TGZ ถูกบันทึกเป็นไฟล์ไบนารีที่บีบอัดโดยใช้อัลกอริธึมการบีบอัด [GZ](/th/compression/gz/)

## วิธีแกะไฟล์ .tgz บน Linux

บน Linux/Unix OS สามารถใช้คำสั่งต่อไปนี้เพื่อคลายไฟล์ TGZ จากบรรทัดคำสั่ง

```
tar zxvf tgzCompressedFile.tgz
```

คำสั่งดังกล่าวจะคลายไฟล์ TGZ ที่ถูกบีบอัดและแตกไฟล์ในไฟล์เก็บถาวร TAR ลงในดิสก์
## อ้างอิง ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

