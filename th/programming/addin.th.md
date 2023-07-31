{
  "date" : "2021-04-22",
  "keywords": [ "addin file", "visual studio addin file", "extension", "format","addin file visual studio","addin file extension","how to open addin file","addin file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADDIN - ไฟล์นิยาม Add-in ของ Visual Studio",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ ADDIN พร้อมตัวอย่างและ API ที่สามารถสร้างและเปิดไฟล์ ADDIN",
  "linktitle" : "ADDIN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-12"
}

## รูปแบบไฟล์ ADDIN คืออะไร?

ไฟล์ที่มีนามสกุล .addin เป็นไฟล์คำจำกัดความของ Add-in ที่สร้างโดย Microsoft Visual Studio สำหรับโครงการ Add-in ใช้สำหรับลงทะเบียน Add-in ใหม่ในตัวจัดการ Add-In ของ Visual Studio IDE เพื่อให้สามารถใช้ในโครงการอื่นโดยไม่ต้องสร้างใหม่ Add-in เป็นแอปพลิเคชันซอฟต์แวร์ขนาดเล็กที่ขยายการทำงานของโปรแกรมที่ใหญ่กว่าโดยไปที่โปรแกรมหลัก ไฟล์ Addin จะถูกจัดเก็บในรูปแบบไฟล์ [XML](/th/web/xml/) ในตำแหน่งเดียวกับที่สร้างโปรเจ็กต์ Add-in

## รูปแบบไฟล์ ADDIN - ข้อมูลเพิ่มเติม

ไฟล์ ADDIN จะถูกบันทึกลงดิสก์ในรูปแบบไฟล์ XML ที่มนุษย์สามารถอ่านได้ สามารถเปิดได้ในโปรแกรมแก้ไขข้อความยอดนิยม เช่น Notepad, Notepad++, Microsoft Visual Studio IDE และอื่นๆ อีกมากมาย Microsoft ได้กำหนด [ไฟล์รายการ XML](https://learn.microsoft.com/en-us/office/dev/add-ins/develop/add-in-manifests?tabs=tabid-1) ของ Office Add -in ที่อธิบายวิธีเปิดใช้งาน Add-in หลังจากติดตั้งและใช้งานกับเอกสารและแอปพลิเคชัน Office

**ดูเพิ่มเติมที่:** [วิธีสร้าง Add-in ของ Office COM โดยใช้ Visual C# .NET](https://learn.microsoft.com/en-us/previous-versions/office/troubleshoot/office-developer /office-com-add-in-using-visual-c)

## อ้างอิง

* [รายการ Office Add-in XML](https://learn.microsoft.com/en-us/office/dev/add-ins/develop/add-in-manifests?tabs=tabid-1)

