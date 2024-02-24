{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ไฟล์ SDF - ไฟล์รูปแบบข้อมูลเชิงพื้นที่",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ SDF และ API ที่สามารถสร้างและเปิดไฟล์ SDF",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf-th",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## ไฟล์ SDF คืออะไร?

A Spatial Data File (SDF) is a Geodatabase file format that was developed by Autodesk. It stores geospatial data and is used by Autodesk GIS program MapGuide and AutoCAD Map 3D. SDF file format is based on the single file database file format SQLite3. ถือเป็นรูปแบบไฟล์ที่ได้รับการปรับปรุงสำหรับชุดข้อมูลเชิงพื้นที่ขนาดใหญ่

คุณสามารถเปิดไฟล์ SDF ได้โดยใช้ Autodesk AutoCAD Map 3D 2022 และ Autodesk AutoCAD Civil 3D 2023

## รูปแบบไฟล์ SDF - ข้อมูลเพิ่มเติม

รูปแบบไฟล์ SDF จะถูกจัดเก็บไว้ในแผ่นดิสก์เป็นไฟล์ไบนารี ขึ้นอยู่กับฐานข้อมูล SQLite ที่ใช้ส่วนประกอบการจัดเก็บข้อมูลระดับต่ำสำหรับการจัดลำดับข้อมูลแบบไบนารี ไฟล์ SDF มีคลาสฟีเจอร์หลายคลาสต่อไฟล์และคุณสมบัติเรขาคณิตหลายรายการสำหรับแต่ละคลาสฟีเจอร์ ข้อมูลในไฟล์ SDF สามารถเข้าถึงได้ด้วยความเร็วสูงเนื่องจากการจัดทำดัชนีคุณสมบัติเรขาคณิตแต่ละรายการโดยใช้ R-tree

## อ้างอิง

* [รูปแบบข้อมูล SDF](https://en.wikipedia.org/wiki/Spatial_Data_File)

* [Importing Autodesk SDF](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

