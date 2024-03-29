{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ AWK - ไฟล์สคริปต์ AWK",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ AWK และ API ที่สามารถสร้างและเปิดไฟล์ AWK",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## ไฟล์ AWK คืออะไร??

ไฟล์ AWK เป็นไฟล์สคริปต์ที่สร้างขึ้นสำหรับแอปพลิเคชันประมวลผลข้อความ **AWK** ที่มาพร้อมกับระบบปฏิบัติการ Unix และ Linux ประกอบด้วยคำแนะนำเชิงตรรกะในการดำเนินการกับข้อความหรือเนื้อหาของไฟล์ เช่น การจับคู่ การแทนที่ และการพิมพ์ข้อความ ซึ่งจะช่วยสร้างรายงานและข้อความที่จัดรูปแบบจากไฟล์อินพุต ยูทิลิตี้ awk มักจะอยู่ใน /usr/bin/awk บนลินุกซ์/ยูนิกซ์ดิสทริบิวชันส่วนใหญ่

## จะสร้างสคริปต์ AWK ได้อย่างไร

ไฟล์ AWK สามารถสร้างหรือเปิดในโปรแกรมแก้ไขข้อความใดก็ได้บน Linux/Unix OS สามารถสร้างไฟล์สคริปต์ AWK ใหม่ได้ดังต่อไปนี้

```
$ vi script.awk
```

นี่จะเป็นการเปิดไฟล์ AWK ในโปรแกรมแก้ไขข้อความ ป้อนคำสั่งบางอย่างในโปรแกรมแก้ไขข้อความดังต่อไปนี้

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
บรรทัดแรกของเนื้อหาข้อความนี้มีคำอธิบายดังต่อไปนี้

* \#! – เรียกว่า `Shebang` ซึ่งระบุล่ามสำหรับคำแนะนำในสคริปต์
* /usr/bin/awk – เป็นล่าม
* -f – ตัวเลือกล่ามใช้ในการอ่านไฟล์โปรแกรม

## วิธีรันสคริปต์ AWK

บันทึกไฟล์และทำให้สคริปต์เรียกใช้งานได้โดยใช้คำสั่งด้านล่าง:
```
$ chmod +x script.awk
```

จากนั้นสามารถรันสคริปต์ได้ดังนี้

```
$ ./script.awk
```

ซึ่งส่งผลให้ผลลัพธ์ต่อไปนี้

```
Writing my first Awk executable script!
```

## อ้างอิง ##

* [เขียนสคริปต์โดยใช้ภาษาโปรแกรม Awk](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

