---
date: 2022-07-30
ผู้เขียน:
  display_name: Kashif Iqbal
draft: false
toc: true
title: รูปแบบไฟล์ JNLP - ไฟล์ JNP คืออะไร??,
linktitle: JNLP
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ JNLP และ API ที่สามารถสร้างและเปิดไฟล์ JNLP"
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## ไฟล์ JNLP คืออะไร??

ไฟล์ JNLP เป็นไฟล์ Java Web Start (JWS) ที่มีข้อมูล XML สำหรับการเรียกใช้โปรแกรม Java ผ่านเครือข่าย บันทึกในรูปแบบ Java Network Launching Protocol (JNLP) ถูกใช้โดยเทคโนโลยี Java Web Start (JWS) ซึ่งเป็นเทคโนโลยีการปรับใช้แอปพลิเคชันเพื่อดาวน์โหลดและเรียกใช้แอปพลิเคชัน ไฟล์ JNLP มีที่อยู่ระยะไกลของเซิร์ฟเวอร์ซึ่งโปรแกรมถูกดาวน์โหลดและเปิดใช้งานบนเครื่องโลคัล

## รูปแบบไฟล์ JNLP - ข้อมูลเพิ่มเติม

ไฟล์ JNLP ถูกบันทึกเป็นไฟล์ **[XML](/th/web/xml/)** ที่จัดเก็บไว้ในรูปแบบข้อความที่มนุษย์อ่านได้ ไฟล์ XML มีข้อมูลที่ใช้ในการเรียกใช้และเรียกใช้แอปพลิเคชัน Java ผ่านเครือข่าย JWS ให้คุณเปิดแอปพลิเคชันโดยคลิกลิงก์หน้าเว็บ มีการดาวน์โหลดแอปพลิเคชันในกรณีที่ยังไม่ได้ดาวน์โหลดบนคอมพิวเตอร์ของผู้ใช้

Oracle เลิกใช้ JWS ด้วยการเปิดตัว Java Platform Standard Edition (JSE) 9 ด้วยเหตุนี้ ไฟล์ JNLP จึงไม่ได้รับการสนับสนุนอีกต่อไป

### วิธีเปิดไฟล์ JNLP

แอปพลิเคชันที่สามารถ **เปิดไฟล์ JNLP** ได้แก่ **Microsoft Visual Studio Code**, **Notepad**, **Notepad*****, **Oracle Java Web Start**, **Karakun OpenWebStart** และ * *GitHub อะตอม**.

### ตัวอย่างไฟล์ JNLP

```
<jnlp spec="1.0" codebase="http://localhost/jws" href="Notepad.jnlp">
   <information>
      <title>Notepad Demo</title>
      <vendor>Sun Microsystems, Inc.</vendor>
   </information>
   <resources>
      <property name="jnlp.publish-url" value="$$context/publish"/>
      <j2se version="1.3+" href="http://java.sun.com/products/autodl/j2se"/>
      <jar href="Notepad.jar"/>
   </resources>
   <application-desc main-class="Notepad"/>
</jnlp>
```
**การใช้งาน**

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<HTML>
<HEAD>
   <TITLE>Java Web Start Demo</TTLE>    
</HEAD>
<BODY>

<H1>Java Web Start Demo</H1>
<a href="Notepad.jnlp">Lanuch Notepad Application</a>
This link is to the Notepad.jnlp file.
</BODY>
</HTML>
```
## วิธีเรียกใช้ไฟล์ JNLP

ด้วยการเลิกใช้งาน JWS แอปพลิเคชันที่พัฒนาโดยใช้เทคโนโลยี JWS ไม่สามารถรันด้วย Java เวอร์ชันล่าสุดได้ อย่างไรก็ตาม โปรแกรมที่ใช้ JNLP เหล่านี้สามารถรันได้โดยใช้ OpenWebStart ซึ่งเป็นการนำเทคโนโลยี Java Web Start มาใช้งานใหม่แบบโอเพ่นซอร์ส ติดตั้งควบคู่ไปกับ Java เวอร์ชันล่าสุดและจัดเตรียมคุณลักษณะที่ใช้บ่อยที่สุดของ Java Web Start และมาตรฐาน JNLP

## อ้างอิง ##

* [Java Web Start คืออะไรและเปิดตัวอย่างไร](https://www.java.com/en/download/help/java_webstart.html)
* [เรียกใช้ JNLP ด้วย Java เวอร์ชันล่าสุด](https://openwebstart.com/)
* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

