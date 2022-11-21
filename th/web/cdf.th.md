{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - รูปแบบคำจำกัดความของช่อง",
  "description" :"เรียนรู้เกี่ยวกับไฟล์ CDF และ API ที่สามารถสร้างและเปิดไฟล์ CDF ได้",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## ไฟล์ CDF คืออะไร??

ไฟล์ที่มีนามสกุล .cdf เป็นรูปแบบไฟล์การเผยแพร่ข้อมูลตาม XLM ซึ่งใช้ในการเผยแพร่การอัปเดตบ่อยครั้งเป็น "ช่อง" ข้อมูลถูกเผยแพร่จากเว็บเซิร์ฟเวอร์ใด ๆ และถูกส่งไปยังคอมพิวเตอร์โดยอัตโนมัติด้วยโปรแกรมรับที่เข้ากันได้ เช่น เว็บเบราว์เซอร์ ผู้ใช้สมัครรับข้อมูลช่องที่ใช้งานอยู่และมีการอัปเดตตามกำหนดเวลาที่ส่งไปยังเดสก์ท็อป
ก่อนหน้านี้ไฟล์ CDF ถูกใช้ร่วมกับเทคโนโลยี Active Channel, Active Desktop และ Smart Offline Favorites ของ Microsoft

## รูปแบบไฟล์ CDF

ไฟล์ CDF ถูกบันทึกเป็นไฟล์ XML ซึ่งเป็นรูปแบบไฟล์เว็บทั่วไปสำหรับการแลกเปลี่ยนข้อมูล รูปแบบไฟล์ CDF เป็นรูปแบบเก่าในขณะนี้และไม่เคยถูกนำมาใช้อย่างแพร่หลาย เมื่อเปรียบเทียบกันแล้ว RSS ของ Netscape นั้นโด่งดังกว่าและใช้กันอย่างแพร่หลาย

### ตัวอย่างรูปแบบไฟล์ CDF

ต่อไปนี้คือตัวอย่างทั่วไปของรูปแบบไฟล์ CDF

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://โดเมน/โฟลเดอร์/"
LASTMOD="1998-11-05T22:12"
PRECACHE="ใช่"
LEVEL="0">
<TITLE>ชื่อช่อง</TITLE>
<ABSTRACT>สรุปเนื้อหาของช่อง</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="ใช่"
LEVEL="1">
<TITLE>ชื่อหน้าสอง</TITLE>
<ABSTRACT>เรื่องย่อเนื้อหาของหน้าสอง</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## อ้างอิง

* [รูปแบบคำจำกัดความของช่อง - โดย Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)

