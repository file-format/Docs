{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "file", "extension", "file format", "Visual C++ Project", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"วีซีเอ็กซ์โปรเจ",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ VCXPROJ และ API ที่สามารถสร้างและเปิดไฟล์ VCXPROJ",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## ไฟล์ VCXPROJ คืออะไร??

ไฟล์ที่มีนามสกุล .vcxproj คือไฟล์โครงการ Microsoft Visual C++ ที่เก็บข้อมูลโครงการ [C++](/th/programming/cpp/) ประกอบด้วยข้อมูลที่ใช้โดยระบบโครงการ MSBuild เพื่อรวบรวมและสร้างผลลัพธ์สุดท้าย VCXPROJ ของโปรเจ็กต์ Visual C++ เหมือนกับของ [CSPROJ](/th/programming/csproj/) สำหรับโปรเจ็กต์ .NET ไฟล์ VCXPROJ ไม่มีโค้ดใดๆ แต่อ้างถึงคลาส เป้าหมาย และคุณสมบัติทั้งหมดที่กำหนดไว้สำหรับโปรเจ็กต์เพื่อสร้างโปรเจ็กต์ สามารถเปิดได้ในโปรแกรมแก้ไขข้อความธรรมดาหรือโดยเฉพาะอย่างยิ่งใน Microsoft Visual Studio IDE


## รูปแบบไฟล์ VCXPROJ - ข้อมูลเพิ่มเติม

ไฟล์ VCXPROJ เป็นไฟล์ข้อความที่สร้างขึ้นในรูปแบบไฟล์ [XML](/th/web/xml/) สามารถเปิดได้ในโปรแกรมแก้ไขข้อความใดๆ แต่ขอแนะนำอย่างยิ่งให้ใช้ Microsoft Visual Studio IDE เพื่อเปิดและแก้ไขไฟล์เหล่านี้ สิ่งเหล่านี้ไม่ได้ออกแบบมาสำหรับการแก้ไขด้วยตนเอง ข้อผิดพลาดอาจทำให้ IDE หยุดทำงานหรือทำงานในลักษณะที่ไม่คาดคิด

เนื้อหาของไฟล์ VCXPROJ ตัวอย่างมีดังต่อไปนี้

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### องค์ประกอบไฟล์ VCXPROJ

ไฟล์ VCXPROJ ทั่วไปมีองค์ประกอบจำนวนหนึ่งดังที่เห็นได้จากตัวอย่าง XML ด้านบน [โครงสร้าง VCXPROJ](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) โดย Microsoft อธิบายองค์ประกอบไฟล์แต่ละรายการโดยละเอียดและสามารถอ้างอิงได้ จากมุมมองของนักพัฒนา

#### องค์ประกอบโครงการ

นี่คือรูทโหนดของไฟล์ VCXPROJ MSBuild ใช้องค์ประกอบนี้เพื่ออ่านเวอร์ชันบิลด์และเป้าหมายเริ่มต้นสำหรับการคอมไพล์

#### องค์ประกอบกลุ่มรายการการกำหนดค่าโครงการ

ประกอบด้วยข้อมูลการกำหนดค่าโครงการที่สามารถรวมวิธีการสร้าง (ดีบักหรือรีลีส) การคอมไพล์ 32 หรือ 64 บิต ตัวเลือกการปรับให้เหมาะสม และอื่นๆ ข้อมูลในกลุ่มนี้ถูกใช้โดย IDE เพื่อโหลดโครงการ

#### องค์ประกอบการกำหนดค่าโครงการ

องค์ประกอบ ProjectConfiguration ในไฟล์ VCXPROJ มีข้อมูลเกี่ยวกับรุ่นและแพลตฟอร์มที่โหลดโครงการ ชื่อควรอยู่ในรูปแบบ `$(Configuration)|$(Platform)`

#### องค์ประกอบ Globals PropertyGroup

ส่วนนี้ประกอบด้วยการตั้งค่าที่ให้ข้อมูลสำหรับระดับโครงการ เช่น:

* ProjectGuid
* รูทเนมสเปซ
* ApplicationType หรือ ApplicationTypeRevision


## อ้างอิง

* [โครงสร้าง VCXPROJ - MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [ไฟล์โครงการ C++](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

