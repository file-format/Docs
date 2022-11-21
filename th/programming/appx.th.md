{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - ไฟล์ APPX คืออะไร",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ APPX และ API ที่สามารถสร้างและเปิดไฟล์ APPX",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## ไฟล์ APPX คืออะไร??

ไฟล์ APPX เป็นรูปแบบไฟล์แพ็คเกจที่สามารถแจกจ่ายได้ซึ่งใช้สำหรับการแจกจ่ายและการติดตั้งแอปพลิเคชัน ได้รับการแนะนำพร้อมกับ Windows 8 เพื่อเผยแพร่บน Microsoft Windows Store ประกอบด้วยไฟล์ทั้งหมดที่จำเป็นสำหรับการติดตั้งแอปพลิเคชัน Windows ซึ่งรวมถึงข้อมูลเมตา ไฟล์ และข้อมูลประจำตัว รูปแบบไฟล์บรรจุภัณฑ์ที่ทันสมัยกว่าคือ MSIX ซึ่งปัจจุบันใช้กันทั่วไปมากกว่าเมื่อเทียบกับ APPX

## รูปแบบไฟล์ APPX - ข้อมูลเพิ่มเติม

ไฟล์ APPX ถูกบันทึกเป็นไฟล์บีบอัดในรูปแบบไฟล์ [ZIP](/th/compression/zip/) ทำให้แพคเกจทั้งหมดเป็นไฟล์เก็บถาวรที่มีขนาดไฟล์ลดลงซึ่งง่ายต่อการอัปโหลดไปยัง Microsoft Store

## จะดูไฟล์ในไฟล์ APPX ได้อย่างไร?

ในการดูเนื้อหาหรือไฟล์ภายในไฟล์ APPX ควรปฏิบัติตามขั้นตอนต่อไปนี้

1. เนื่องจากไฟล์ APPX ถูกจัดเก็บเป็นไฟล์ ZIP ที่ถูกบีบอัด ให้เปลี่ยนชื่อไฟล์เป็นนามสกุล .zip
1. ใช้เครื่องมือคลายการบีบอัด เช่น 7-Zip, WinZip หรือ WinRAR เพื่อแตกไฟล์ที่อยู่ในไฟล์ APPX

## วิธีสร้างไฟล์ APPX

มีสองวิธีที่สามารถใช้ในการสร้างไฟล์ APPX

1. การใช้ MakeApp.exe - ใช้ [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) เพื่อสร้างทั้งสองอย่าง แพ็กเกจแอป (.msix หรือ .appx) และไฟล์แพ็กเกจแอป .msixbundle หรือ .appxbundle) นอกจากนี้ยังสามารถแยกไฟล์จากแพ็คเกจแอพ MakeApp.exe พร้อมใช้งานกับ Windows 10 SDK และสามารถใช้งานได้จากพรอมต์คำสั่ง
1. การใช้ Microsoft Visual Studio - นักพัฒนามักจะ [สร้างไฟล์ APPX](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) โดยใช้ Microsoft Visual Studio เมื่อการพัฒนาแอปพลิเคชันเสร็จสิ้นและแอปพร้อมที่จะเผยแพร่แล้ว คุณสามารถสร้างไฟล์แพ็คเกจ APPX ได้โดยการเผยแพร่จากภายใน Visual Studio

## อ้างอิง

* [สร้างแพ็คเกจ MSIX หรือบันเดิลด้วย MakeAppx.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [สร้างไฟล์ APPX โดยใช้ Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

