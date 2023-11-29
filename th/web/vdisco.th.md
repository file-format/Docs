{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ VDISCO - รูปแบบไฟล์เอกสาร DISCO Dynamic Discovery",
  "description":"เรียนรู้ว่าไฟล์ VDISCO คืออะไร",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## ไฟล์ VDISCO คืออะไร??

ไฟล์ VDISCO เป็นไฟล์การค้นพบที่ Microsoft Visual Studio ใช้ในบริการบนเว็บ โดยให้ข้อมูลเกี่ยวกับบริการบนเว็บที่มีอยู่ เช่น URL เนมสเปซ และวิธีการ ไฟล์ VDISCO คล้ายกับรูปแบบไฟล์ [DISCO](/th/web/disco/) แต่ถูกสร้างขึ้นที่รันไทม์ มันถูกเก็บไว้ในแอปพลิเคชันบริการเว็บและถูกใช้โดย Visual Studio เพื่อค้นหาและใช้บริการเว็บในโครงการแบบไดนามิก ไฟล์ VDISCO ใช้ร่วมกับไฟล์ [.asmx](/th/web/asmx/) ที่มีรหัสบริการเว็บจริง

คุณสามารถเปิดไฟล์ VDISCO ในโปรแกรมแก้ไขข้อความใดก็ได้ เช่น Microsoft Notepad, Github Atom และ Apple TextEdit นอกจากนี้ยังสามารถเปิดด้วย Microsoft Visual Studio 2012 และใหม่กว่าเพื่อใช้งานได้

## รูปแบบไฟล์ VDISCO

ไฟล์ VDISCO จะถูกบันทึกและโฮสต์ในรูปแบบไฟล์ [XML](/th/web/xml/) ซึ่งเป็นรูปแบบสากลสำหรับการจัดองค์ประกอบและการเผยแพร่ข้อมูล ประกอบด้วย URL บริการ เนมสเปซ และวิธีการในแท็ก XML มาตรฐาน โดยแต่ละแท็กมีค่าของข้อมูลตามลำดับ

## อ้างอิง

* [ดิสโก้](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [การค้นพบบริการเว็บ](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [ตัวอย่าง C# ของคลาส DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

