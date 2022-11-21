---
date: 2022-05-09
ผู้เขียน:
  display_name: Kashif Iqbal
draft: false
toc: true
title: รูปแบบไฟล์ PYM - ไฟล์พรีโปรเซสเซอร์มาโคร PYM,
linktitle: PYM
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ PYM และ API ที่สามารถสร้างและเปิดไฟล์ PYM"
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## ไฟล์ PYM คืออะไร??

ไฟล์ PYM เป็นไฟล์มาโครพรีโพรเซสเซอร์ตามภาษาโปรแกรม Python ได้รับการพัฒนาโดย VRVis Research และจัดเก็บทางลัดมาโคร เมื่อไฟล์ PYM ถูกตีความโดยขั้นตอนการประมวลผลล่วงหน้าของล่าม Python ทางลัดเหล่านี้จะถูกขยายเพื่อแทนที่ข้อความแบบเต็ม นอกจากนี้ การดำเนินการทางเลือกที่สามที่สามารถทำได้โดยตัวประมวลผลล่วงหน้าแมโครคือการรวมไฟล์ ไฟล์ PYM สามารถเปิดได้ในโปรแกรมแก้ไขข้อความ เช่น Notepad, Notepad++, Apple TextEdit และ VI บน Linux

## รูปแบบไฟล์ PYM

ไฟล์ PYM ถูกบันทึกเป็นไฟล์ข้อความล้วนลงแผ่นดิสก์ ไฟล์ PYM ยังสามารถรวมไฟล์อื่นๆ โดยใช้คำสั่ง `#include`

### ไวยากรณ์ PYM

คำสั่ง PYM จะรวมอยู่ระหว่างเครื่องหมาย ""#begin python และ "#end python" ดังที่แสดงด้านล่าง

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### การขยายมาโคร PYM

การขยายมาโคร PYM แสดงด้วยสองลำดับ ได้แก่ <[ และ ]> นี่คือแท็ก html พิเศษและสามารถปรากฏที่ใดก็ได้ในบรรทัด ตัวอย่าง PYM เล็กน้อยมีดังนี้

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

ผลลัพธ์ของการรันสิ่งนี้ผ่าน PYM เป็นดังนี้:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## อ้างอิง ##

* [PYM - ตัวประมวลผลล่วงหน้ามาโครที่ใช้ Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [ล่าม PYM](https://github.com/interpreters/pym)

