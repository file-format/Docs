{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "เชลล์สคริปต์ - วิธีรันบน Ubuntu และ Linux",
  "description":"เรียนรู้เกี่ยวกับ Shell Script คืออะไร และวิธีการรันบน Ubuntu และ Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-th",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## เชลล์สคริปต์คืออะไร?

การเขียนสคริปต์เชลล์เกี่ยวข้องกับการเขียนชุดคำสั่งในไฟล์ข้อความธรรมดา ซึ่งมักเรียกว่า **เชลล์สคริปต์** สคริปต์เหล่านี้ดำเนินการโดยเชลล์ซึ่งเป็นล่ามบรรทัดคำสั่ง เปลือกหอยที่พบมากที่สุด ได้แก่

1. Bash (บอร์นอีกครั้งเชลล์)
2. Zsh (Z เชลล์)
3. ปลา.

เชลล์สคริปต์มีได้ตั้งแต่บรรทัดเดียวธรรมดาไปจนถึงโปรแกรมที่ซับซ้อน และใช้เพื่อทำงานที่หลากหลาย เช่น การจัดการไฟล์ การดูแลระบบ และการทำงานอัตโนมัติของงานที่ซ้ำกัน

## ประโยชน์ของการเขียนสคริปต์เชลล์:

1.  **การทำงานอัตโนมัติ:** เชลล์สคริปต์ช่วยให้ผู้ใช้ทำงานที่ซ้ำกันโดยอัตโนมัติ ประหยัดเวลา และลดโอกาสที่จะเกิดข้อผิดพลาดจากมนุษย์
    
2.  **การปรับแต่ง:** ผู้ใช้สามารถสร้างสคริปต์ที่ปรับให้เหมาะกับความต้องการเฉพาะของตนเองได้ โดยให้การปรับแต่งในระดับสูง
    
3.  **การประมวลผลเป็นชุด:** เชลล์สคริปต์เหมาะอย่างยิ่งสำหรับการจัดการงานการประมวลผลเป็นชุด ซึ่งจำเป็นต้องดำเนินการหลายคำสั่งตามลำดับ
    
4.  **การดูแลระบบ:** โดยทั่วไปจะใช้เชลล์สคริปต์สำหรับงานการดูแลระบบ เช่น การสำรองข้อมูล การหมุนเวียนบันทึก และการติดตั้งซอฟต์แวร์

## การเขียนสคริปต์เชลล์อย่างง่าย:

มาสร้างเชลล์สคริปต์พื้นฐานที่พิมพ์ข้อความทักทายกัน เปิดโปรแกรมแก้ไขข้อความและสร้างไฟล์ชื่อ `greeting.sh` เพิ่มบรรทัดต่อไปนี้:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

บันทึกไฟล์และทำให้สามารถเรียกใช้งานได้โดยการรันคำสั่งต่อไปนี้ในเทอร์มินัล:

```
chmod +x greeting.sh
```

ตอนนี้คุณสามารถรันสคริปต์ได้:

```
./greeting.sh
```

ผลลัพธ์ควรเป็น:

```
Hello, welcome to the world of shell scripting!
```

## การรันเชลล์สคริปต์บน Ubuntu และ Linux:

ตอนนี้ เราจะมาพูดถึง **วิธีเรียกใช้ไฟล์ .sh ใน Ubuntu และ Linux**

1.  **ทำให้สคริปต์ทำงานได้:** ก่อนที่จะเรียกใช้เชลล์สคริปต์ ตรวจสอบให้แน่ใจว่าสคริปต์นั้นสามารถเรียกใช้งานได้ ใช้คำสั่ง `chmod` ดังที่แสดงไว้ก่อนหน้านี้
    
2.  **นำทางไปยังไดเรกทอรีสคริปต์:** เปิดเทอร์มินัลแล้วใช้คำสั่ง `cd` เพื่อไปยังไดเรกทอรีที่มีเชลล์สคริปต์ของคุณ
    
3.  **เรียกใช้สคริปต์:** เรียกใช้สคริปต์โดยพิมพ์ `./scriptname.sh` ในเทอร์มินัล โดยแทนที่ scriptname ด้วยชื่อจริงของสคริปต์ของคุณ
    
```
cd path/to/script
./greeting.sh
``` 

4.  **การใช้คำสั่ง Bash:** หากสคริปต์ของคุณขึ้นต้นด้วย `#!/bin/bash` (เรียกว่า **shebang**) คุณยังสามารถรันสคริปต์โดยใช้คำสั่ง `bash` ได้อีกด้วย

```
bash greeting.sh
```

## $@ หมายถึงอะไรในเชลล์สคริปต์

ในเชลล์สคริปต์ `$@` แสดงถึงอาร์กิวเมนต์บรรทัดคำสั่งทั้งหมดที่ส่งไปยังสคริปต์ มักใช้เพื่ออ้างอิงรายการอาร์กิวเมนต์เป็นเอนทิตีที่แยกจากกัน เมื่อใช้ภายในเครื่องหมายคำพูดคู่ เช่น `$@` จะรักษาอาร์กิวเมนต์แต่ละรายการ โดยคำนึงถึงช่องว่างและอักขระพิเศษ

นี่คือคำอธิบายสั้น ๆ:

- `$@`: แสดงถึงพารามิเตอร์ตำแหน่งทั้งหมด (อาร์กิวเมนต์) ที่ส่งผ่านไปยังสคริปต์หรือฟังก์ชัน อาร์กิวเมนต์แต่ละรายการจะถือเป็นคำที่แยกจากกัน
    
- `$@`: เมื่อมีการใช้เครื่องหมายคำพูดคู่ จะคงการแยกอาร์กิวเมนต์ไว้ โดยอนุญาตให้มีการเว้นวรรคหรืออักขระพิเศษภายในอาร์กิวเมนต์แต่ละรายการ
    

นี่คือตัวอย่างง่ายๆ ที่จะแสดง:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

เมื่อคุณรันสคริปต์นี้พร้อมกับอาร์กิวเมนต์ เช่น:

```
bash example.sh arg1 "argument 2" arg3
```

มันจะส่งออก:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

อย่างที่คุณเห็น `$@` แสดงถึงอาร์กิวเมนต์ทั้งหมด และ `$@` จะคงอาร์กิวเมนต์แต่ละรายการไว้ แม้ว่าจะมีช่องว่างก็ตาม

