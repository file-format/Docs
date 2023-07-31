{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - ไฟล์อ้างอิงมาโคร Microsoft Office",
  "description":"เรียนรู้เกี่ยวกับไฟล์ MSO และ API ที่สามารถสร้างและเปิดไฟล์ MSO",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## ไฟล์ MSO คืออะไร??

ไฟล์ MSO เป็นรูปแบบไฟล์คอนเทนเนอร์ข้อมูลที่สร้างขึ้นเมื่อส่งข้อความ HTML โดยใช้ Microsoft Outlook สิ่งนี้เกิดขึ้นกับแอปพลิเคชัน Microsoft Office 2000 เป็นส่วนใหญ่ ในกรณีส่วนใหญ่ ข้อความอีเมลจะแนบมาพร้อมกับชื่อไฟล์ **Oledata.mso** ผู้รับอีเมลเมื่อเปิดอีเมลดังกล่าว สามารถดูไฟล์ได้อย่างถูกต้องแม้ว่าจะไม่ได้ติดตั้งซอฟต์แวร์เดียวกันก็ตาม ไฟล์ MSO อ้างถึง [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

## รูปแบบไฟล์ Microsoft MSO

ไฟล์ MSO จะถูกบันทึกในรูปแบบไฟล์ Microsoft Compound Document File Format (MCDF) ซึ่งเรียกอีกอย่างว่า Object Linking and Embedding (OLE) หรือ Component Object Model (COM) โครงสร้างการจัดเก็บไฟล์คอมโพเนนต์รูปแบบไฟล์ไบนารี

### โครงสร้างรูปแบบไฟล์ MSO

โครงสร้างรูปแบบไฟล์ภายในของรูปแบบไฟล์ MSO มีการกำหนดไว้อย่างดีใน [โครงสร้าง](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) ส่วนของเอกสาร MCDF ตารางการจัดสรรไฟล์ (FAT) จัดการการจัดสรรเซกเตอร์และเชนเซกเตอร์ ประกอบด้วยอาร์เรย์ของหมายเลขเซกเตอร์ 32 บิต แต่ละดัชนีในอาร์เรย์แสดงถึงหมายเลขเซกเตอร์ ในขณะที่ค่าของมันแสดงถึงเซกเตอร์ถัดไปในห่วงโซ่หรือค่าพิเศษ

## อ้างอิง

* [พื้นที่จัดเก็บที่มีโครงสร้าง COM](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [รูปแบบไฟล์เอกสารประกอบของ Microsoft (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

