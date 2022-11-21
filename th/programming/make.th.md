{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"สร้างไฟล์ - ไฟล์สคริปต์ Xcode Makefile",
  "description":"เรียนรู้เกี่ยวกับรูปแบบ XCode MakeFile และ API ที่สามารถสร้างและเปิดไฟล์ MakeFile",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## ไฟล์ MAKE คืออะไร??

ไฟล์ MAKE เป็นไฟล์สคริปต์ XCode ที่จัดระเบียบการคอมไพล์โค้ด ใช้เพื่อคอมไพล์และเชื่อมโยงโปรแกรมจากไฟล์ซอร์สโค้ดหลายไฟล์ ช่วยในการตัดสินใจว่าส่วนใดของแอปพลิเคชันขนาดใหญ่จำเป็นต้องคอมไพล์ใหม่เมื่อจำเป็นต้องอัปเดตแอปพลิเคชัน ทำให้ไฟล์ใช้ชุดคำสั่งในการทำงานขึ้นอยู่กับว่าไฟล์ใดมีการเปลี่ยนแปลง

## สร้างตัวอย่างรูปแบบไฟล์

เนื้อหาต่อไปนี้ดำเนินการโดยใช้ยูทิลิตี Make และเอาต์พุตมีดังต่อไปนี้

```
hello:
	echo "hello world"
```
**สร้างผลผลิต**

```
$ make
echo "hello world"
hello world
```

## อ้างอิง
* [XCode and Make - ฟอรัม Apple](https://developer.apple.com/forums/thread/657458)
* [คู่มือ Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

