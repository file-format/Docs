---
date: 2019-10-11
keywords: prc, .prc, รูปแบบไฟล์ prc, วิธีเปิดไฟล์ prc, นามสกุล .prc, นามสกุล prc,
ผู้เขียน:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: รูปแบบไฟล์ PRC,
linktitle: PRC
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ PRC และ API ที่สามารถสร้างและเปิดไฟล์ PRC"
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## รูปแบบไฟล์ PRC
มีการใช้ส่วนขยาย ".prc" สำหรับรูปแบบไฟล์ Product Representation Compact 3D และรูปแบบไฟล์ e-book โดย MobiPocket

## ไฟล์ Product Representation Compact (PRC) คืออะไร

PRC (Product Representation Compact) คือรูปแบบไฟล์ 3 มิติที่ได้รับการปรับแต่งเพื่อจัดเก็บ โหลด และแสดงข้อมูล 3 มิติ โดยเฉพาะอย่างยิ่งที่มาจากระบบ CAD (การออกแบบโดยใช้คอมพิวเตอร์ช่วย) เป็นไฟล์ไบนารีแบบลำดับ เขียนด้วยวิธีแบบพกพา สามารถใช้ PRC เพื่อฝังข้อมูล 3 มิติในไฟล์ PDF PRC รองรับโครงสร้างหลักส่วนใหญ่ของ CAD เช่น แอสเซมบลีและชิ้นส่วน ต้นไม้ของเอนทิตี 3 มิติ การแสดงรูปทรงเรขาคณิตที่แน่นอน การแสดงรูปสามเหลี่ยม และมาร์กอัป PRC ใช้นามสกุล .prc และประเภทสื่ออินเทอร์เน็ตที่ใช้คือ *model/prc*

PRC เป็นรูปแบบไฟล์อเนกประสงค์ที่ขึ้นอยู่กับการใช้งาน สามารถจัดเก็บโดยใช้การบีบอัดปกติเพื่อแสดงข้อมูล CAD โดยตรง หรือจัดเก็บโดยใช้การบีบอัดสูงเพื่อลดขนาดไฟล์ ข้อมูล 3 มิติที่จัดเก็บไว้ใน PDF โดยใช้รูปแบบ PRC สามารถทำงานร่วมกันได้กับแอปพลิเคชัน CAM และ CAE

### ข้อกำหนดรูปแบบไฟล์ Product Representation Compact (PRC)

ไฟล์ PRC มีส่วนหัวหลักหนึ่งส่วนตามด้วยโครงสร้างไฟล์อย่างน้อยหนึ่งไฟล์ตามด้วยไฟล์โมเดลหนึ่งไฟล์ที่ส่วนท้าย โครงสร้างไฟล์มีหนึ่งส่วนหัวตามด้วยส่วนข้อมูลต่อไปนี้:

- **Globals**: ประกอบด้วยโครงสร้างไฟล์และสีที่อ้างอิง ลักษณะเส้น และระบบพิกัดสำหรับเอนทิตีทรีแต่ละรายการของโครงสร้างไฟล์
- **Tree**: ประกอบด้วยคำอธิบายแผนภูมิของรายการ เช่น การเกิดขึ้นของผลิตภัณฑ์ คำจำกัดความของชิ้นส่วน รายการตัวแทน และมาร์กอัป
- **Tessellation**: ประกอบด้วยข้อมูล tessellated(triangulated) ทั้งหมดในเอนทิตี leaf ของ tree (รายการตัวแทนและมาร์กอัป)
- **เรขาคณิต**: ประกอบด้วยข้อมูลเรขาคณิตและโทโพโลยีที่แน่นอนทั้งหมดของเอนทิตีลีฟของทรี (รายการตัวแทน)
- **รูปทรงเรขาคณิตพิเศษ**: ประกอบด้วยข้อมูลสรุปของรูปทรงเรขาคณิต ซึ่งช่วยให้โหลดไฟล์ได้บางส่วนโดยไม่ต้องโหลดรูปทรงเรขาคณิตทั้งหมด

ต่อไปนี้เป็นโครงสร้างของไฟล์ PRC ทั่วไป

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## ไฟล์ e-book MobiPocket ที่มีนามสกุล PRC คืออะไร
รูปแบบไฟล์ e-book ซึ่งเปิดตัวโดยบริษัทฝรั่งเศสชื่อ **Mobipocket** ก็ใช้นามสกุล ".prc" เช่นกัน ในขั้นต้น Mobipocket ได้เปิดตัวแอปพลิเคชันฟรีสำหรับอุปกรณ์อัจฉริยะหลายตัว เช่น แท็บเล็ตพีซี พีดีเอ และสมาร์ทโฟน ส่วนขยาย ".prc" จริง ๆ แล้วเหมือนกับ .mobi แต่ใช้เฉพาะกับพีดีเอที่รองรับเฉพาะส่วนขยาย **.prc** หรือ **.pdb**

### ข้อกำหนดรูปแบบไฟล์ Mobipocket PRC
รูปแบบไฟล์ MobiPocket PRC เป็นไปตามมาตรฐาน Open eBook โดยใช้ XHTML และยังสามารถรวม JavaScript และเฟรมได้อีกด้วย รองรับการสืบค้น SQL ดั้งเดิมที่จะใช้กับฐานข้อมูลแบบฝังตัว

Mobipocket Reader มีไลบรารีโฮมเพจ ผู้อ่านสามารถแทรกหน้าว่างในส่วนใดก็ได้ของหนังสือและเพิ่มภาพวาดตัวแปร วัตถุต่างๆ เช่น คำอธิบายประกอบ ที่คั่นหน้า การแก้ไข บันทึก และภาพวาดสามารถจัดการได้จากที่เดียว รูปภาพจะถูกแปลงเป็นรูปแบบ GIF และมีขนาดสูงสุด 64K ซึ่งเพียงพอสำหรับโทรศัพท์มือถือที่มีหน้าจอขนาดเล็ก Mobipocket Reader มีที่คั่นหน้าอิเล็กทรอนิกส์และพจนานุกรมในตัว

เครื่องอ่านมีโหมดเต็มหน้าจอสำหรับการอ่านและรองรับพีดีเอ เครื่องมือสื่อสาร และสมาร์ทโฟนจำนวนมาก ผลิตภัณฑ์ Mobipocket รองรับระบบปฏิบัติการ Palm, Windows, Symbian, BlackBerry ส่วนใหญ่ แต่ไม่รองรับ Android เครื่องอ่านทำงานภายใต้ Linux หรือ Mac OS X โดยใช้ WINE

## อ้างอิง

- [สาธารณรัฐประชาชนจีน - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [ข้อกำหนดรูปแบบ PRC](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [การเปรียบเทียบรูปแบบ e-book - โดย Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

