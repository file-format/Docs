{
  "date" : "2021-12-01",
  "keywords" :[ "gnm", "file", "extension", "file format", "gnumeric", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"ไฟล์ GNM และ API ที่สามารถสร้างและเปิดไฟล์ GNM คืออะไร",
  "title" :"GNM - รูปแบบไฟล์สเปรดชีต Gnumeric",
  "linktitle" : "GNM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-12-01"
}

## ไฟล์ GNM คืออะไร??

ไฟล์ GNM เป็นไฟล์สเปรดชีตที่สร้างด้วย [Gnumeric](https://en.wikipedia.org/wiki/Gnumeric) ซึ่งเป็นโปรแกรมสเปรดชีตและมาเป็นส่วนหนึ่งของ [GNOME](https://www.gnome.org/) Desktop ซอฟต์แวร์. โดยจะเก็บข้อมูลสเปรดชีตเป็นแถวและคอลัมน์ และให้การสนับสนุนแผนภูมิและฟังก์ชันสเปรดชีตอื่นๆ ไฟล์ GNM ถูกบันทึกลงดิสก์ในรูปแบบไฟล์ [XML](/th/web/xml/) (คล้ายกับ XLSX) และถูกบีบอัดโดยใช้ [GZIP](/th/compression/gz/) จุดมุ่งหมายของ Gnumeric คือการจัดหาแอปพลิเคชันสเปรดชีตโอเพ่นซอร์สซึ่งจะเป็นทางเลือกแทน Microsoft Excel ในที่สุด

## รูปแบบไฟล์ GNM

ไฟล์ GNM เป็นไฟล์ XML ที่ถูกบีบอัดที่สามารถแตกไฟล์ได้ด้วยยูทิลิตี้คลายการบีบอัดมาตรฐาน เช่น WinZIP แม้ว่าจะมีคุณสมบัติมากมาย แต่ Gnumic ไม่รองรับ Macros และ Pivot Tables

## คุณสมบัติที่รองรับในไฟล์ GNM

เนื่องจาก Gnumeric รองรับไฟล์รูปแบบต่างๆ จึงสามารถแปลงไฟล์ GNM ดั้งเดิมเป็น [CSV](/th/spreadsheet/csv/), [XLSX](/th/spreadsheet/xlsx/), Microsoft Works (.wks), [HTML](/th/web/html/), [LaTex](/th/word-processing/latex/) และ [Lotus 1-2-3](/th/spreadsheet/123/)

## Gnumeric บน Github

การพัฒนาแบบโอเพ่นซอร์สของ Gnumeric โฮสต์และดูแลบนที่เก็บ [Gnumeric official Github](https://github.com/GNOME/gnumeric)

## อ้างอิง

* [โครงการ GNOME](https://en.wikipedia.org/wiki/The_GNOME_Project)
* [Gnumeric - โดย Wikipedia](https://en.wikipedia.org/wiki/Gnumeric)

