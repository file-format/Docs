{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "รูปแบบไฟล์", "ไฟล์ pak คืออะไร", "ไฟล์", "ตัวอย่าง pak", "ไฟล์แพ็คเกจวิดีโอเกม","นามสกุล"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับไฟล์ .pak และ API ที่สามารถสร้างและเปิดไฟล์ PAK",
  "title" :"รูปแบบไฟล์ PAK- ไฟล์แพ็คเกจวิดีโอเกม",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## ไฟล์ PAK คืออะไร??

ไฟล์ PAK เป็นไฟล์แพ็คเกจที่สร้างขึ้นโดยวิดีโอเกมต่าง ๆ เพื่อเก็บข้อมูลเกม โดยพื้นฐานแล้วมันเป็นรูปแบบไฟล์เกม ซึ่งอาจรวมถึงองค์ประกอบต่างๆ ของเกม เช่น กราฟิก พื้นผิว เสียง วัตถุ และข้อมูลเกมอื่นๆ ไฟล์เก็บถาวรส่วนใหญ่จะบันทึกเป็นไฟล์ .zip และสามารถแตกไฟล์ได้ด้วยซอฟต์แวร์บีบอัดยอดนิยม เช่น WinZip และ WinRAR ตัวอย่างของวิดีโอเกมที่ใช้ไฟล์ PAK ได้แก่ Quake, Hexen, Crysis และ Half-Life

## รูปแบบไฟล์ PAK - ข้อมูลเพิ่มเติม

ในกรณีส่วนใหญ่ ไฟล์ PAK จะถูกบันทึกใน [รูปแบบไฟล์ ZIP](/th/compression/zip/) แต่แอปพลิเคชันที่แตกต่างกันอาจใช้รูปแบบไฟล์ที่แตกต่างกันในการจัดเก็บไฟล์เหล่านี้


## วิธีการเปิดไฟล์ PAK?

คุณสามารถเปิดไฟล์ PAK ด้วยแอปพลิเคชัน เช่น [PakExplorer](https://www.quaketerminus.com/tools.shtml) และ [SpriteExplorer](http://www.slackiller.com/hlprograms.htm)

**------------------------------------------------ -------------------------------------------------- -----------------------**

## รูปแบบไฟล์ PAK - ไฟล์วัตถุ Simutrans

ไฟล์ที่มีนามสกุล .pak เป็นรูปแบบไฟล์เกมจำลองการขนส่งของ [Simutrans](https://www.simutrans.com/en/) ประกอบด้วยวัตถุที่ใช้ในการจำลอง เช่น กราฟิกที่ผู้ใช้สร้างขึ้นและเนื้อหาข้อมูล สามารถมีวัตถุต่างๆ มากมาย เช่น ยานพาหนะในเกม อาคาร ภูมิประเทศ และอื่นๆ ไฟล์ PAK สร้างขึ้นโดยใช้ MakeObject ซึ่งเป็นยูทิลิตี้ที่รวบรวมไฟล์ .dat และรูปภาพ .png เพื่อสร้างวัตถุจำลองเหล่านี้ Simutrans ให้ผู้เล่นใช้ระบบขนส่งที่ประสบความสำเร็จโดยสร้างและจัดการระบบการขนส่งสำหรับผู้โดยสาร ไปรษณีย์ และสินค้าทางบก

## จะสร้างไฟล์ PAK ได้อย่างไร?

Simutrans ได้แสดงรายการตัวอย่างสำหรับการสร้างไฟล์ PAK บน Windows และ Linux OS

### ระบบปฏิบัติการ Windows

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### ลินุกซ์ BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## อ้างอิง

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)