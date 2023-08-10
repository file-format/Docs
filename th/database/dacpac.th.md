{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "extension", "file", "file format", "Database File Type", "Database File Format", "Data Tier AppliCation Package" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ DACPAC และ API ที่สามารถสร้างและเปิดไฟล์ DACPAC",
  "title" :"DACPAC - แพ็คเกจการสมัคร Data Tier",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## ไฟล์ DACPAC คืออะไร??

ไฟล์ที่มีนามสกุล .dacpac (ย่อมาจาก Data Tier AppliCation Package) คือไฟล์ฐานข้อมูลที่สร้างขึ้นด้วยแอปพลิเคชัน Data Tier ของ Microsoft SQL Server ซึ่งมีโมเดลฐานข้อมูลสำหรับการแสดงวัตถุฐานข้อมูล เนื่องจากมีโมเดลฐานข้อมูลที่สมบูรณ์ จึงใช้เพื่อกู้คืนฐานข้อมูลจากรายละเอียดที่มีอยู่ในโมเดล โดยปกติไฟล์ DACPAC จะถูกส่งต่อไปยังทีมปรับใช้สำหรับการติดตั้งในสถานที่ของลูกค้าเพื่อกู้คืนฐานข้อมูล สามารถเปิดได้ด้วย
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## รูปแบบไฟล์ DACPAC - ข้อมูลเพิ่มเติม

ไฟล์แพ็คเกจข้อมูล DACPAC เป็นไฟล์ ZIP ที่ถูกบีบอัดซึ่งมีไฟล์ [XML](/th/web/xml/) หลายไฟล์ที่มีข้อมูลเกี่ยวกับโมเดลฐานข้อมูล เช่น ตารางและมุมมอง ซึ่งใช้ในการกู้คืนฐานข้อมูล หากต้องการดูเนื้อหาของไฟล์ DACPAC ให้เปลี่ยนชื่อไฟล์จาก .dacpac เป็น [.zip](/th/compression/zip/) และแตกไฟล์ zip โดยใช้ยูทิลิตีคลายการบีบอัด

ต่อไปนี้คือไฟล์บางส่วนที่พบในไฟล์ DACPAC

* [Content_Types].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>ซีอาร์เอ็ม</Name>
<Version>1.0.0.0</Version>
</DacType>
```
*Origin.xml

* model.xml

โปรดทราบว่า DACPAC ไม่มี DATA และวัตถุระดับเซิร์ฟเวอร์อื่นๆ ไฟล์สามารถมีวัตถุทุกประเภทซึ่งอาจเก็บไว้ในโครงการ SSDT

## อ้างอิง

* [แอปพลิเคชันระดับข้อมูล - ประโยชน์](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications?view=sql-server-ver15)
* [การปรับใช้แอปพลิเคชัน Data Tier - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [วิธีสร้างไฟล์ DACPAC](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

