{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ gpx", "ไฟล์ gpx คืออะไร", "ไฟล์", "ตัวอย่าง gpx", "นามสกุลไฟล์ gpx", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - รูปแบบไฟล์แลกเปลี่ยน GPX",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ GPX และ API ที่สามารถสร้างและเปิดไฟล์ GPX",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ GPX คืออะไร??

ไฟล์ที่มีนามสกุล GPX แสดงถึงรูปแบบการแลกเปลี่ยน GPS สำหรับการแลกเปลี่ยนข้อมูล GPS ระหว่างแอปพลิเคชันและบริการบนเว็บบนอินเทอร์เน็ต เป็นรูปแบบไฟล์ XML น้ำหนักเบาที่มีข้อมูล GPS เช่น จุดอ้างอิง เส้นทาง และแทร็กที่จะนำเข้าและแดงโดยหลายโปรแกรม รูปแบบไฟล์ GPX เปิดอยู่และรองรับโดยแอพพลิเคชั่นและอุปกรณ์ GPS ที่หลากหลาย สามารถโหลดข้อมูล GPS จากไฟล์ดังกล่าวเพื่อแสดงบนแอปพลิเคชันแผนที่เพื่อวัตถุประสงค์เชิงพื้นที่

## รูปแบบไฟล์ GPX ##

ไฟล์ GPX ประกอบด้วยข้อมูลตำแหน่งละติจูดและลองจิจูด ค่าระดับความสูง และข้อมูลเชิงอธิบายอื่นๆ ข้อมูลตำแหน่งจะแสดงเป็นองศาทศนิยมและระดับความสูงจะแสดงเป็นเมตร เวลาในไฟล์ GPX เป็นเวลาสากลเชิงพิกัด (UTC) โดยใช้รูปแบบ ISO 8601 ประโยชน์ของการใช้ไฟล์ GPX มีดังนี้:

* GPX ช่วยให้คุณสามารถแลกเปลี่ยนข้อมูลกับรายการโปรแกรมที่เพิ่มขึ้นสำหรับ Windows, MacOS, Linux, Palm และ PocketPC
* GPX สามารถแปลงเป็นรูปแบบไฟล์อื่นได้โดยใช้เว็บเพจหรือโปรแกรมแปลงอย่างง่าย
* GPX ขึ้นอยู่กับมาตรฐาน XML ดังนั้นโปรแกรมใหม่จำนวนมากที่คุณใช้ (เช่น Microsoft Excel) สามารถอ่านไฟล์ GPX ได้
* GPX ช่วยให้ทุกคนบนเว็บสามารถพัฒนาคุณสมบัติใหม่ที่จะทำงานร่วมกับโปรแกรมโปรดของคุณได้ทันที

[GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) แสดงรูปแบบไฟล์ GPX สำหรับอ้างอิง

### ข้อมูลสำคัญ ###

ต่อไปนี้เป็นข้อมูลสำคัญที่เป็นส่วนหนึ่งของไฟล์ GPX สำหรับการแสดงข้อมูล GPS

* **เวย์พอยต์**: เวย์พอยต์คือพิกัด WGS84 (GPS) ของจุดและแสดงถึงเลเยอร์ของฟีเจอร์ประเภท OGR wkbPoint
* **เส้นทาง**: แสดงเลเยอร์ของคุณสมบัติประเภท OGR wkbLineString ประกอบด้วยรายการจุดติดตาม ซึ่งเป็นจุดอ้างอิงที่แสดงทางเลี้ยวหรือจุดที่เวทีซึ่งนำไปสู่จุดหมาย
* **แทร็ก**: แทร็กแสดงถึงเลเยอร์ของฟีเจอร์ประเภท OGR wkbMultiLineString มันถูกสร้างขึ้นจากอย่างน้อยหนึ่งส่วนที่มีเวย์พอยต์ในรายการลำดับของจุดที่อธิบายถึงเส้นทาง ประกอบด้วยรายการจุดติดตามซึ่งแสดงถึงรอยทาง GPS ที่ต่อเนื่องกัน

### ไฟล์ตัวอย่าง GPX ###

ไฟล์ GPX ต่อไปนี้แสดงการจัดระเบียบข้อมูล GPS ในไฟล์ GPX และสามารถให้แนวคิดที่ดีเกี่ยวกับเนื้อหาของไฟล์ GPX

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## อ้างอิง ##

* [รูปแบบไฟล์ GPX](http://www.topografix.com/gpx.asp)
* [GPX - โดย Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

