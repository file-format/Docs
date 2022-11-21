
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์โฆษณา - รูปแบบไฟล์ข้อมูลจำเพาะของ Ada",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ ADS พร้อมตัวอย่างและ API ที่สามารถสร้างและเปิดไฟล์ ADS ได้",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## ไฟล์ ADS คืออะไร??

ไฟล์ ADS เป็นไฟล์ข้อมูลจำเพาะสำหรับโครงการเขียนโปรแกรม Ada ซึ่งคล้ายกับคลาสสำหรับ Java หรือคู่ของส่วนหัวและการใช้งานในกรณีของ C++ ข้อกำหนดสาธารณะและส่วนตัวของแพ็คเกจ Ada ถูกจัดเก็บไว้ในไฟล์ .ads ในทางตรงกันข้าม ไฟล์ .adb มีการใช้งานหรือเนื้อหาของ Ada เช่นเดียวกับ [C++](/th/programming/cpp/) Ada นำเสนอการแยกระหว่างข้อมูลจำเพาะและการใช้งานโดยไม่ขึ้นกับ OOP

ไฟล์ ADS สามารถเปิดได้ในโปรแกรมแก้ไขข้อความใดๆ เช่น Microsoft Notepad, Notepad++ และ Atom

## รูปแบบไฟล์โฆษณา

ไฟล์ ADS อยู่ในรูปแบบไฟล์ข้อความธรรมดาอย่างง่าย และสามารถเปิด/แก้ไขได้ด้วยโปรแกรมแก้ไขข้อความใดๆ แพ็คเกจ Ada สามารถจัดระเบียบเป็นลำดับชั้นได้ หน่วยย่อยสามารถประกาศได้ด้วยวิธีต่อไปนี้:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## อ้างอิง

* [แพ็คเกจ Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

