{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ NUPKG - ไฟล์แพ็คเกจ NuGet",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ NUPKG และ API ที่สามารถสร้างและเปิดไฟล์ NUPKG",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## ไฟล์ NUPKG คืออะไร??

ไฟล์ NUPKG เป็นไฟล์แพ็คเกจที่มีซอร์สโค้ดที่จะใช้โดยซอฟต์แวร์ NuGet สำหรับสร้างแพ็คเกจที่จะใช้ในโครงการ .NET คอมโพเนนต์ NuGet Package Manager ได้รับการติดตั้งเป็นส่วนหนึ่งของ Microsoft Visual Studio สำหรับการดึงแพ็กเกจจากที่เก็บโฮสต์แพ็กเกจออนไลน์ ไฟล์ NUPKG ช่วยให้นักพัฒนาดึงแพ็คเกจล่าสุดจาก [Nuget.org](https://nuget.org) โดยใช้ NuGet Package Manager แทนการดาวน์โหลดและติดตั้งแพ็คเกจการพัฒนาด้วยตนเอง ไฟล์ NUPKG สร้างขึ้นจากไฟล์ NUSPEC และเมื่อดึงข้อมูลแล้ว ให้ติดตั้งแพ็คเกจบนระบบผู้ใช้

## รูปแบบไฟล์ NUPKG

ไฟล์ NUPKG เป็นไฟล์เก็บถาวร [ZIP](/th/compression/zip/) ที่มีไลบรารีที่บรรจุอยู่ภายใน เมื่อดาวน์โหลดแล้ว สามารถเปลี่ยนชื่อเป็น .zip และแตกไฟล์ด้วยยูทิลิตี้ zip มาตรฐานใดก็ได้ เช่น WinZIP, 7-Zip และ Apple Archive Utility

## อ้างอิง

* [Nuget.org](https://nuget.org)
* [การเริ่มต้นอย่างรวดเร็ว: ติดตั้งและใช้แพ็คเกจใน Visual Studio (Windows เท่านั้น)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- สตูดิโอ)
* [วิธีสร้างและเผยแพร่แพ็คเกจ Nuget](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- คลิ)

