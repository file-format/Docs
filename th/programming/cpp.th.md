{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "ไฟล์", "นามสกุล", "รูปแบบไฟล์", "C++", "ภาษาโปรแกรม" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ซอร์สโค้ด CPP - C++",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CPP และ API ที่สามารถสร้างและเปิดไฟล์ CPP",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ C++ คืออะไร?

ไฟล์ที่มีนามสกุลไฟล์ CPP คือไฟล์ซอร์สโค้ดสำหรับแอปพลิเคชันที่เขียนด้วยภาษาโปรแกรม C++ โครงการ C++ เดียวอาจมีไฟล์ CPP มากกว่าหนึ่งไฟล์เป็นซอร์สโค้ดของแอปพลิเคชัน โปรเจ็กต์ดังกล่าวประกอบด้วยไฟล์ประเภทต่างๆ ซึ่งไฟล์ CPP เรียกว่าไฟล์การใช้งาน เนื่องจากมีคำจำกัดความทั้งหมดของเมธอดที่ประกาศไว้ในไฟล์ส่วนหัว (.h) โครงการ C ++ โดยรวมส่งผลให้แอปพลิเคชันปฏิบัติการเมื่อคอมไพล์ทั้งหมด

## โครงสร้างไฟล์ CPP

โครงสร้างไฟล์ CPP นั้นเรียบง่ายเมื่อเทียบกับไฟล์ส่วนหัว วัตถุประสงค์หลักของไฟล์การใช้งานดังกล่าวคือเพื่อแยกส่วนต่อประสานออกจากการใช้งาน ส่งผลให้มีการประกาศฟังก์ชันสมาชิกทั้งหมดในไฟล์ส่วนหัวและรายละเอียดภายในไฟล์ CPP ไฟล์การใช้งาน CPP สามารถใช้เป็นไฟล์อย่างง่ายสำหรับการเขียนแอปพลิเคชันหรือเป็นการใช้งานคลาส

### การดำเนินการอย่างอิสระ

ไฟล์ CPP เมื่อใช้เป็นแอ็พพลิเคชันอิสระสามารถมีการใช้งานทั้งหมดอยู่ภายในโดยไม่ต้องมีการประกาศเมธอดในไฟล์ส่วนหัว การใช้งานดังกล่าวประกอบด้วยวิธีการทั้งหมดที่กำหนดไว้ในไฟล์การใช้งานที่รายการของแอปพลิเคชันถูกควบคุมโดยวิธีการหลักที่รับอินพุตของผู้ใช้เพิ่มเติมเป็นอาร์กิวเมนต์ นอกจากนี้ยังสามารถรวมไลบรารีใดๆ จากไลบรารีมาตรฐาน C++ ที่จะใช้โดยวิธีการใดๆ ที่ประกาศไว้ในไฟล์

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### การใช้งานคลาส

ในการเขียนโปรแกรมเชิงวัตถุ (OOP) ไฟล์ CPP ใช้เป็นข้อกำหนดของคลาส ในกรณีเช่นนี้ สมาชิกข้อมูลคลาสและฟังก์ชันสมาชิกทั้งหมดจะถูกประกาศภายในไฟล์ส่วนหัว ไฟล์ส่วนหัวแต่ละไฟล์สามารถอ้างอิงถึงวิธีการไลบรารีมาตรฐานได้เช่นกัน ไฟล์ CPP คำจำกัดความของคลาสอ้างถึงไฟล์ส่วนหัวในคำสั่งรวมที่จุดเริ่มต้นของไฟล์ ส่วนใหญ่แล้ว นักพัฒนาซอฟต์แวร์จะรวมความคิดเห็นไว้ที่จุดเริ่มต้นของไฟล์การใช้งานคลาสดังกล่าว ซึ่งให้ข้อมูลเกี่ยวกับเนื้อหาจริงของไฟล์ รายละเอียดของผู้เขียน และวันที่ใช้งาน ในกรณีดังกล่าว ไฟล์การใช้งานส่วนหัวต้องมีชื่อเดียวกัน ตัวอย่างของส่วนหัวและไฟล์การใช้งานมีดังนี้

### ไฟล์ส่วนหัว

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### ไฟล์การดำเนินการ CPP

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## อ้างอิง

* [การใช้งานคลาส - โดย Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)
