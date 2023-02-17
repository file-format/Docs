{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ xpm", "รูปแบบไฟล์ xpm", "ไฟล์ xpm คืออะไร", "ไฟล์", "ตัวอย่าง xpm", "นามสกุลไฟล์ xpm", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ XPM - X PixMap",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ XPM และ API ที่สามารถสร้างและเปิดไฟล์ XPM",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ XPM คืออะไร??

ไฟล์ที่มีนามสกุล .xpm เป็นรูปแบบไฟล์ภาพที่ระบบ X Windows ใช้ สนับสนุนพิกเซลแบบโปร่งใสและมักจะกำหนดเป้าหมายการสร้างไอคอน pixmaps รองรับข้อมูลขาวดำ gra-scale และ color pixmap สิ่งเหล่านี้ได้รับการออกแบบมาให้สามารถแก้ไขได้ด้วยมือและสามารถรวมอยู่ในโค้ด [C](/th/programming/c/) เพื่อจุดประสงค์นี้ ไฟล์ XPM จะอยู่ในรูปแบบไฟล์ข้อความธรรมดาและเป็นไปตามไวยากรณ์ของภาษาโปรแกรม C ไฟล์ XPM สามารถเปิดได้ด้วยแอปพลิเคชั่นดูภาพที่หลากหลายเช่น
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView และ Canvas X

## รูปแบบไฟล์ XPM

รูปแบบไฟล์ XPM ใช้ไวยากรณ์ C เพื่อให้สิ่งเหล่านี้รวมอยู่ในโปรแกรม C และ C ++ ประกอบด้วยหกส่วนที่แตกต่างกันดังต่อไปนี้

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

ส่วนต่าง ๆ เป็นอาร์เรย์ของสตริงดังต่อไปนี้

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
ต่อไปนี้เป็นรายละเอียดของแต่ละส่วน

`<Values> ` - ส่วนนี้เป็นสตริงที่มีจำนวนเต็มสี่หรือหกตัวที่อยู่ในฐาน 10 และสอดคล้องกับ:

* ความกว้างและความสูงของ pixmap
* จำนวนสี
* จำนวนตัวอักษรต่อพิกเซล
* พิกัดฮอตสปอตเสริมและแท็ก XPMEXT

`<Colors> ` - ส่วนนี้มีสตริงมากเท่าที่มีสี แต่ละสตริงมีดังนี้:

```
<chars>{<key><color> }+
```
`<Pixels> ` - ส่วนนี้ประกอบด้วย<height> สตริงและ<width> \*<chars_per_pixel> ตัวละคร ทั้งหมด<chars_per_pixel> สตริงความยาวควรเป็นหนึ่งในกลุ่มที่กำหนดไว้ก่อนหน้านี้ใน<Colors> ส่วน.

`<Extension> ` - ส่วนส่วนขยายต้องมีป้ายกำกับ หากไม่ว่างเปล่า ให้อยู่ใน<Values> ส่วน. อาจประกอบด้วยหลาย<Extension> ส่วนย่อยซึ่งอาจเป็นสองประเภทต่อไปนี้:

* หนึ่งสตริงแบบสแตนด์อโลนที่ประกอบด้วยดังนี้: XPMEXT<extension-name><extension-data>
* หรือบล็อกที่ประกอบด้วยหลายสตริง:XPMEXT<extension-name><related extension-data composed of several strings>

## อ้างอิง

* [XPM - วิกิพีเดีย](https://en.wikipedia.org/wiki/X_PixMap)
* [คู่มือ XPM](http://www.xfree86.org/current/xpm.pdf)
