{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "file", "extension", "file format", "CSharp", "Programming Language" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์รหัส CS - CSharp",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CS และ API ที่สามารถสร้างและเปิดไฟล์ CS",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ CS คืออะไร??

ไฟล์ที่มีนามสกุล .cs เป็นไฟล์ซอร์สโค้ดสำหรับภาษาโปรแกรม C# รูปแบบไฟล์นี้เปิดตัวโดย Microsoft เพื่อใช้กับ .NET Framework ซึ่งเป็นภาษาการเขียนโปรแกรมระดับต่ำสำหรับการเขียนโค้ดที่คอมไพล์เพื่อสร้างไฟล์ผลลัพธ์สุดท้ายในรูปแบบของ EXE หรือ DLL สิ่งเหล่านี้สามารถสร้างและคอมไพล์ด้วย Microsoft Visual Studio นอกจากนี้ยังสามารถใช้ Microsoft Visual Studio Express เพื่อสร้างและอัปเดตไฟล์ดังกล่าวซึ่งเป็น IDE ฟรี ไฟล์ CS ใช้สำหรับการพัฒนาแอปพลิเคชันที่มีตั้งแต่แอปพลิเคชันเดสก์ท็อปธรรมดาไปจนถึงโปรแกรมที่ซับซ้อนมากขึ้น โครงการ Visual Studio อย่างง่าย [โซลูชัน](/th/programming/sln/) ที่สร้างด้วยภาษา C# สามารถประกอบด้วยไฟล์ดังกล่าวตั้งแต่หนึ่งไฟล์ขึ้นไป ไฟล์ที่ทำเครื่องหมายให้รวมอยู่ในการคอมไพล์จะแสดงอยู่ในไฟล์ [CSPROJ](/th/programming/csproj/) ซึ่งเป็นส่วนหนึ่งของโปรเจ็กต์และบอกให้คอมไพเลอร์ใช้ไฟล์ที่ทำเครื่องหมาย

## รูปแบบไฟล์ CS ##

ไฟล์ CS เป็นรูปแบบไฟล์ข้อความที่สามารถเปิดในโปรแกรมแก้ไขข้อความเพื่อแก้ไข อย่างไรก็ตาม เมื่อเปิดใน IDE ที่รองรับด้วยการเน้นไวยากรณ์ที่เหมาะสม โค้ดจะอ่านและจัดเรียงได้ง่าย ไฟล์ CS อย่างง่ายประกอบด้วย:

* การประกาศเนมสเปซ - สำหรับการอ้างอิงถึงฟังก์ชันเฉพาะที่กำหนดโดยเนมสเปซเฉพาะนั้น
* การประกาศตัวแปร - เพื่อประกาศตัวแปรระดับคลาสสำหรับการใช้งานเฉพาะ
* การประกาศเมธอด - เพื่อประกาศการประกาศเมธอดสำหรับการทำงานเฉพาะ

### ไวยากรณ์ ###

* เครื่องหมายอัฒภาคใช้เพื่อระบุจุดสิ้นสุดของคำสั่ง
* วงเล็บปีกกาใช้เพื่อจัดกลุ่มคำสั่ง โดยทั่วไปคำสั่งจะจัดกลุ่มเป็นเมธอด (ฟังก์ชัน) เมธอดในคลาส และคลาสในเนมสเปซ
* ตัวแปรกำหนดโดยใช้เครื่องหมายเท่ากับ แต่เปรียบเทียบโดยใช้เครื่องหมายเท่ากับสองตัวติดกัน
* วงเล็บเหลี่ยมใช้กับอาร์เรย์ ทั้งเพื่อประกาศและรับค่าที่ดัชนีที่กำหนดในหนึ่งในนั้น

### ตัวอย่าง ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```
