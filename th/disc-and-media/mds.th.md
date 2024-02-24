{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "เรียนรู้เกี่ยวกับรูปแบบไฟล์ MDS และ API ที่สามารถสร้างและเปิดไฟล์ MDS",
  "title" : "รูปแบบไฟล์ MDS - ไฟล์ Sidecar ของตัวอธิบายสื่อ",
  "linktitle" : "MDS",
  "menu" : {
    "docs" : {
      "identifier":"disc-and-media-mds-th",
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2023-01-23"
}

## ไฟล์ MDS คืออะไร??

MDS (ไฟล์ Media Descriptor Sidecar) เป็นไฟล์ที่เกี่ยวข้องกับซอฟต์แวร์ Alcohol 120% และ Daemon Tools ซึ่งทั้งสองอย่างนี้ใช้สำหรับสร้างและจัดการไดรฟ์ซีดีและดีวีดีเสมือน ไฟล์ MDS มีข้อมูลเกี่ยวกับเค้าโครงของข้อมูลบนแผ่นดิสก์ รวมถึงตำแหน่งของไฟล์ทั้งหมดและโครงสร้างของแผ่นดิสก์ ซึ่งช่วยให้ไดรฟ์เสมือนจำลองการทำงานของดิสก์จริงได้ เพื่อให้ซอฟต์แวร์สามารถอ่านข้อมูลบนดิสก์เสมือนได้เสมือนว่าเป็นดิสก์จริง

When you want to mount an image file to a virtual drive, the MDS file is used along with the corresponding image file in a format such as ISO, BIN or CUE. The MDS file contains a description of the layout of the data on the disc, and the virtual drive software uses this information to create a virtual disc. This allows you to use the software as if you were using a physical disc, without having to physically insert the disc into the drive.

## ความสัมพันธ์กับแอลกอฮอล์ 120%

Alcohol 120% เป็นซอฟต์แวร์ยอดนิยมสำหรับการสร้างและจัดการไดรฟ์ซีดีและดีวีดีเสมือน และใช้รูปแบบไฟล์ MDS เพื่อบันทึกและเข้าถึงอิมเมจของดิสก์ รูปแบบไฟล์ MDS เป็นกรรมสิทธิ์ของ Alcohol 120% และสามารถเปิดและใช้งานได้โดยซอฟต์แวร์ Alcohol 120% หรือซอฟต์แวร์อื่นที่รองรับเท่านั้น

## เปิดไฟล์ .MDS ได้อย่างไร

หากต้องการเปิดไฟล์ MDS ใน Alcohol 120% คุณจะต้องติดตั้งซอฟต์แวร์บนคอมพิวเตอร์ของคุณ เมื่อคุณติดตั้ง Alcohol 120% แล้ว คุณสามารถเปิดไฟล์ MDS ได้โดยทำดังนี้:

1. เปิดตัวแอลกอฮอล์ 120%
2. คลิกที่เมนู ไฟล์ และเลือก เปิด
3. นำทางไปยังตำแหน่งของไฟล์ MDS บนคอมพิวเตอร์ของคุณแล้วเลือก
4. ตอนนี้ไฟล์ MDS จะถูกเปิดใน Alcohol 120% และคุณจะได้รับแจ้งให้เลือกไฟล์รูปภาพที่เกี่ยวข้อง (เช่น ISO, BIN หรือ CUE)
5. หลังจากที่คุณเลือกไฟล์ภาพแล้ว Alcohol 120% จะเมานต์ภาพไปยังไดรฟ์เสมือน

หรือคุณสามารถเปิดไฟล์ MDS ได้โดยดับเบิลคลิกที่ไฟล์นั้น หากตั้งค่า Alcohol 120% เป็นโปรแกรมเริ่มต้นสำหรับเปิดไฟล์ MDS คุณยังสามารถใช้ซอฟต์แวร์อื่นที่รองรับรูปแบบ MDS เช่น Daemon Tools, Virtual CloneDrive, Virtual Drive Manager และ MagicISO

## อ้างอิง
* [Alcohol 120% - ซอฟต์แวร์เบิร์นซีดีและดีวีดี](https://www.alcohol-soft.com/)


