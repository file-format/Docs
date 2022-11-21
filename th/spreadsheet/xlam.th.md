---
date: 2019-12-10
keywords: xlam, .xlam, รูปแบบไฟล์ xlam, รูปแบบไฟล์ .xlam, นามสกุล .xlam,
ผู้เขียน:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ XLAM และ API ที่สามารถสร้างและเปิดไฟล์ XLAM"
title: รูปแบบไฟล์ XLAM,
linktitle: XLAM
menu:
  docs:
    parent: "spreadsheet"
lastmod: 2021-06-01
---

## ไฟล์ XLAM คืออะไร?? ##

XLAM เป็นไฟล์ Add-In ที่เปิดใช้งานมาโครซึ่งใช้เพื่อเพิ่มฟังก์ชันใหม่ให้กับสเปรดชีต Add-In คือโปรแกรมเสริมที่รันโค้ดเพิ่มเติมและจัดเตรียมฟังก์ชันเพิ่มเติมสำหรับสเปรดชีต ไฟล์ XLAM ถูกจัดเก็บด้วยนามสกุล .xlam ไฟล์ XLAM เป็นไฟล์ที่ใช้ XML ซึ่งคล้ายกับรูปแบบไฟล์ [XLSM](/th/spreadsheet/xlsm/) และ [XLSX](/th/spreadsheet/xlsx/) และบันทึกด้วยการบีบอัด ZIP เพื่อลดขนาดไฟล์โดยรวม

### ตัวอย่าง ###

```cmd
Public Function Add(num1 As Double, num2 As Double)
Add = num1 + num2
End Function
```

หลังจากนี้ ให้บันทึกไฟล์ด้วยนามสกุล .xlam

## อ้างอิง ##

- [การอ้างอิงรูปแบบไฟล์ - ](https://docs.microsoft.com/en-us/deployoffice/compat/office-file-format-reference)

