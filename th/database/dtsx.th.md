{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "นามสกุล", "ไฟล์", "รูปแบบไฟล์", "ประเภทไฟล์ฐานข้อมูล", "รูปแบบไฟล์ฐานข้อมูล", "ไฟล์ฐานข้อมูล" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ DTSX และ API ที่สามารถสร้างและเปิดไฟล์ DTSX",
  "title" :"รูปแบบไฟล์ DTSX - ไฟล์การตั้งค่า SQL Server DTS",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## ไฟล์ DTSX คืออะไร??

ไฟล์ที่มีนามสกุล .dtsx (Data Transformation Services Package XML) คือไฟล์ Data Transformation Services (DTS) ที่ Microsoft SQL ใช้เพื่ออ้างถึงขั้นตอน/กฎการย้ายข้อมูลสำหรับการถ่ายโอนข้อมูลจากฐานข้อมูลหนึ่งไปยังอีกฐานข้อมูลหนึ่ง ซึ่งรวมถึงการแปลงและขั้นตอนการประมวลผลเพิ่มเติมที่อาจจำเป็นในระหว่างการถ่ายโอนข้อมูลระหว่างจุดเริ่มต้นและปลายทาง SQL Server Integration Services (SSIS) ซึ่งเป็นส่วนประกอบของ Microsoft SQL Server ใช้ไฟล์ DTSX เพื่อระบุขั้นตอนในการประมวลผลข้อมูลระหว่างเซิร์ฟเวอร์ฐานข้อมูล ไฟล์ DTSX สามารถเปิดได้ด้วย Microsoft SQL Server 2019

## รูปแบบไฟล์ DTSX

การเคลื่อนย้ายข้อมูลระหว่างเซิร์ฟเวอร์ฐานข้อมูลจำเป็นต้องมีกฎและขั้นตอนการประมวลผลเพื่อให้แน่ใจว่าข้อมูลมีความสมบูรณ์ในระหว่างการดำเนินการนี้ SSIS ช่วยให้มั่นใจได้ว่ากิจกรรมเหล่านี้ทั้งหมด เพื่อย้ายและปรับข้อมูลจากแหล่งต่างๆ ในองค์กร ดำเนินไปอย่างสะดวกสบาย นั่นคือที่มาของ DTSX ที่กำหนดโครงสร้างที่จะใช้โดย SSIS เพื่อสร้างขั้นตอนที่สามารถประมวลผลข้อมูลได้เมื่อทำตามขั้นตอนเหล่านี้

กระแสข้อมูลอธิบายโดย DTSX ดังแสดงในภาพต่อไปนี้

{{< figure src="../DataFlowDTSX.png" alt="การไหลของข้อมูล DTSX" >}}

DTSX เป็นแบบ [XML](/th/web/xml/) และได้รับการบันทึกไว้ใน [MS-DTSX](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13- 4b5b-a388-aa3c65aec1dd). การปรับโครงสร้างขั้นสูงของ DTSX XML คือ DTSX 2.0 ที่มีแอตทริบิวต์ใหม่ให้กับโครงสร้าง การแทนที่คุณสมบัติที่มีชื่อเป็นแอตทริบิวต์ XML หลัก ระบุค่าเริ่มต้นสำหรับค่าแอตทริบิวต์ส่วนใหญ่ และการวางองค์ประกอบซ้ำภายในองค์ประกอบหลัก มีการอธิบายโครงสร้าง DTSX โดยใช้ [XML Schema](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) เหล่านี้ และรูปแบบโครงสร้างคือ XML ข้อความ celar

## อ้างอิง

* [รูปแบบ DTSX - Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [รูปแบบ DTSX 2 - โดย Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

