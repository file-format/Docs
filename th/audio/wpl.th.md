{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "ไฟล์ wpl", "นามสกุล", "รูปแบบ", "ไฟล์ wpl คืออะไร", "เพลง", "รูปแบบไฟล์ wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ WPL และ API ที่สามารถสร้าง แปลง และเปิดไฟล์ WPL",
  "title" :"WPL - ไฟล์เพลย์ลิสต์ Windows Media Player",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## ไฟล์ WPL คืออะไร??

ไฟล์ที่มีนามสกุล .wpl มีเพลย์ลิสต์ของเพลงที่จะเรียกใช้บน Microsoft Windows Media Player ไฟล์เหล่านี้มักจะสร้างโดยผู้ใช้สำหรับคอลเลกชันวิดีโอและเสียง เนื้อหาที่เขียนในไฟล์ WPL เป็นเพียงเส้นทางไดเร็กทอรีหรือตำแหน่งของไฟล์มัลติมีเดียที่เลือกโดยผู้สร้างไฟล์ .wpl ดังนั้นแอปพลิเคชันเครื่องเล่นสื่อจึงสามารถค้นหาและเล่นเนื้อหามัลติมีเดียจากตำแหน่งไดเร็กทอรีได้ทันที

## รูปแบบไฟล์ WPL

WPL (Windows Media Player Playlist) เป็นรูปแบบไฟล์ที่เป็นกรรมสิทธิ์ซึ่งใช้ใน Microsoft Windows Media Player เวอร์ชัน 9 หรือสูงกว่า เป็นรูปแบบไฟล์คอมพิวเตอร์ที่เก็บรายการเล่นมัลติมีเดีย ตามค่าเริ่มต้น เพลย์ลิสต์จะถูกบันทึกด้วยนามสกุล .wpl (Windows Media Player Playlist) คุณสามารถใช้ส่วนขยาย [.m3u](/th/audio/m3u) แทนได้ หากคุณต้องการเล่นดิสก์ข้อมูลในอุปกรณ์ที่ไม่รองรับส่วนขยายนี้ องค์ประกอบของไฟล์ WPL แสดงในรูปแบบ XML

องค์ประกอบระดับบนสุด "smil" ระบุว่าองค์ประกอบของไฟล์เป็นไปตามโครงสร้าง Synchronized Multimedia Integration Language (SMIL) ไฟล์ถูกสร้างและบันทึกด้วยนามสกุล .wpl และประเภท MIME ของมันคือ application/vnd.ms-wpl

### ตัวอย่าง WPL

นี่คือตัวอย่างของไฟล์ wpl:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>,
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## อ้างอิง ##

* [MPEG-1 Audio Layer II - โดย Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

