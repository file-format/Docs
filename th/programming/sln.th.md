{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"เอสแอลเอ็น",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ SLN และ API ที่สามารถสร้างและเปิดไฟล์ SLN",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ SLN คืออะไร??
ไฟล์ที่มีนามสกุล .SLN แสดงถึงไฟล์ **โซลูชัน Visual Studio** ที่เก็บข้อมูลเกี่ยวกับการจัดระเบียบโครงการไว้ในไฟล์โซลูชัน เนื้อหาของไฟล์โซลูชันดังกล่าวเขียนด้วยข้อความล้วนภายในไฟล์ และสามารถสังเกต/แก้ไขได้โดยการเปิดไฟล์ในโปรแกรมแก้ไขข้อความใดๆ ข้อมูลที่อยู่ในไฟล์โซลูชันจะคงอยู่และใช้เพื่อโหลดข้อมูลที่เกี่ยวข้องกับโซลูชัน เช่น [projects ](/th/programming/csproj/)และข้อมูลที่จำเป็นอื่นๆ ไฟล์โครงการที่อ้างอิงโดยไฟล์โซลูชันมีข้อมูลเพิ่มเติมเพื่อเปิดใช้งานสภาพแวดล้อมสำหรับการเติมลำดับชั้นด้วยรายการของโครงการนั้น ไม่มีการจัดเก็บข้อมูลในไฟล์ .sln แม้ว่าข้อมูลโครงการสามารถเขียนลงในไฟล์ .sln ได้หากจำเป็น

## **ประวัติเวอร์ชัน SLN** ##

เวอร์ชันรูปแบบโซลูชันได้รับการพัฒนาขึ้นพร้อมกับโซลูชัน Microsoft Visual Studio แต่ละรายการเมื่อเวลาผ่านไป รายละเอียดเกี่ยวกับสิ่งเหล่านี้มีดังต่อไปนี้


|เวอร์ชัน Visual Studio|เวอร์ชันรูปแบบโซลูชัน
---|---|
|2546|8.00 น
|2548|9.00
|2551|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **เนื้อหาของไฟล์โซลูชัน** ###

ไฟล์โซลูชันประกอบด้วยหลายส่วนที่สภาพแวดล้อมอ่านเพื่อโหลดโครงการ ตัวอย่างเนื้อหาไฟล์ .sln มีดังต่อไปนี้

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **ประกาศโครงการ** ###

ไฟล์โซลูชันสามารถมีการประกาศโครงการมากกว่าหนึ่งโครงการและประเภทโครงการที่แตกต่างกันได้ ตัวอย่างเช่น ไฟล์โซลูชันเดียวสามารถมี CSharp และโปรเจ็กต์ VB.NET ประเภทเหล่านี้มีความแตกต่างในโซลูชันโดยใช้ [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs) ประกาศโครงการข้างต้นสามารถสรุปได้ดังต่อไปนี้เพื่อความเข้าใจที่ชัดเจน

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID นั้นไม่ซ้ำกันสำหรับประเภทโครงการต่างๆ และถูกใช้โดยตัวอ่านโซลูชันเพื่อระบุประเภทของโครงการ ในกรณีนี้ F184B08F-C81C-45F6-A57F-5ABD9991F28F แสดงว่าเป็นโครงการ VB.NET

`Project GUID:` GUID เฉพาะของโครงการที่ทำให้แตกต่างจากโครงการอื่นๆ ในโซลูชัน รหัสเฉพาะของโครงการในโซลูชันทำให้โครงการอื่นๆ ในโซลูชันสามารถเข้าถึงได้

ตามข้อมูลที่มีอยู่ในส่วนโครงการของไฟล์ .sln สภาพแวดล้อมจะโหลดแต่ละไฟล์โครงการ ตัวโครงการเองมีหน้าที่รับผิดชอบในการเติมลำดับชั้นของโครงการและโหลดโครงการที่ซ้อนกัน การเปลี่ยนแปลงใด ๆ ที่ทำกับโซลูชันจะถูกบันทึกกลับไปยังไฟล์โซลูชันเมื่อบันทึกหรือปิดโครงการ

## โซลูชัน Visual Studio VS โครงการ

**โครงการ:** ตามหลักเหตุผลแล้ว เมื่อคุณเริ่มสร้างแอปหรือซอฟต์แวร์โดยใช้ Visual Studio แสดงว่าคุณเริ่มโครงการใหม่ โปรเจ็กต์ประกอบด้วยไฟล์ที่จำเป็นทั้งหมด เช่น ซอร์สโค้ด ไอคอน รูปภาพ ไฟล์ข้อมูล และอื่นๆ ซึ่งจะถูกคอมไพล์เป็นแอปปฏิบัติการ เว็บไซต์ หรือไลบรารี

**วิธีแก้ปัญหา:** โซลูชันประกอบด้วยหนึ่งโครงการขึ้นไป ดังนั้นวิธีแก้ปัญหาก็เหมือนกับคอนเทนเนอร์สำหรับโครงการ Visual Studio ตามเหตุผลแล้ว เราสามารถพูดได้ว่ามีคนต้องการโซลูชันที่สมบูรณ์สำหรับธุรกิจของเขา ซึ่งรวมถึงเว็บไซต์ แอปบนเดสก์ท็อป บริการเพื่อการพักผ่อน และแอปบนอุปกรณ์เคลื่อนที่

### **ข้อมูลอ้างอิง** ###

* [ไฟล์โซลูชัน - โดย MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [GUID ประเภทโครงการ](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

