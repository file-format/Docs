{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ EGG - ไฟล์การแจกจ่าย Python",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ EGG และ API ที่สามารถสร้างและเปิดไฟล์ EGG",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## ไฟล์ EGG คืออะไร??

ไฟล์ EGG หรือที่เรียกว่า Python egg เป็นรูปแบบการแจกจ่าย Python ที่เก่ากว่า เป็นไฟล์เก็บถาวรแบบบีบอัด [ZIP](/th/compression/zip/) ที่มีนามสกุล .egg และมีไฟล์ต้นฉบับของแอปพลิเคชัน Python พร้อมกับข้อมูลเมตาเกี่ยวกับการแจกจ่าย ไฟล์ EGG เป็นทางเลือกแทนไฟล์ Windows Executable [EXE](/th/executable/exe/) แต่เป็นไฟล์ข้ามแพลตฟอร์ม รูปแบบเก่านี้สำหรับการแจกแจง Python ถูกแทนที่ด้วยรูปแบบไฟล์ Wheel (WHL) ที่ใหม่กว่าในต้นปี 2010

## รูปแบบไฟล์ EGG

ไฟล์ EGG จะถูกบันทึกเป็นไฟล์บีบอัด ZIP หมายความว่าหากคุณแทนที่ส่วนขยาย .egg ด้วย .zip คุณจะสามารถเปิดได้ด้วยยูทิลิตี้คลายการบีบอัดมาตรฐาน เช่น Corel WinZIP, Microsoft Explorer หรือ RARLAB WinRAR

ไฟล์ EGG สามารถสร้างได้โดยใช้แพ็คเกจ **distutils** ที่มีให้โดย Python เครื่องมืออื่นที่สามารถสร้างและเปิดไฟล์ EGG คือ **SetupTools** ไฟล์ EGG สามารถติดตั้งเป็นแพ็คเกจได้โดยใช้ **easy_install**

`หมายเหตุ - รูปแบบไฟล์ EGG ล้าสมัยแล้วเนื่องจากรูปแบบไฟล์ WHL ล้อใหม่'

## อ้างอิง ##

* [Python EGG](https://python101.pythonlibrary.org/chapter38_eggs.html)

