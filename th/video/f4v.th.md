---
date: 2019-10-11
keywords: f4v, .f4v, รูปแบบไฟล์ f4v, รูปแบบไฟล์ .f4v, นามสกุล .f4v, นามสกุล f4v, รูปแบบวิดีโอ f4v, วิธีเปิดไฟล์ f4v, ไฟล์ f4v คืออะไร,
ผู้เขียน:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ F4V และ API ที่สามารถสร้างและเปิดไฟล์ F4V"
title: รูปแบบไฟล์ F4V,
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## ไฟล์ F4V คืออะไร?? ##

F4V (ไฟล์วิดีโอ Flash MP4) เป็นไฟล์วิดีโอที่บันทึกด้วยนามสกุล .f4v เป็นไปตามรูปแบบไฟล์มีเดียฐาน ISO (MPEG-4 ตอนที่ 12) คล้ายกับ [MP4](/th/video/mp4/) มาก ซึ่งเป็นสาเหตุที่เรียกอย่างไม่เป็นทางการว่า Flash MP4 [FLV](/th/video/flv/) มีข้อจำกัดเมื่อสตรีมเนื้อหา H.264/ACC ซึ่งส่งผลให้ Adobe Systems สร้างรูปแบบ F4V ใหม่ Flash Player สามารถเล่นไฟล์ F4V ได้ตั้งแต่เปิดตัว Flash Player 9 Update 3

## โครงสร้างของไฟล์ F4V ##

รูปแบบไฟล์ F4V อิงตามรูปแบบไฟล์มีเดียฐาน ISO (MPEG-4 ตอนที่ 12) และคล้ายกับรูปแบบ MP4 มาก สำหรับรายละเอียดเกี่ยวกับโครงสร้าง โปรดดูที่หน้า [MP4](/th/video/mp4/) ข้อแตกต่างที่สำคัญระหว่าง F4V และ MP4 คือรูปแบบข้อมูลเมตาที่ F4V สามารถจัดเก็บได้ ด้านล่างนี้เป็นรายการรูปแบบข้อมูลเมตาที่สนับสนุนโดยรูปแบบ F4V

- **กล่องแท็ก**: กล่องแท็กเพิ่มเติมสี่กล่อง (auth, title, dscp, cprt) ภายในกล่อง Movie (moov)
- **ช่องข้อมูลเมตา XMP**: ช่องนี้อยู่หลังช่อง Movie (moov) ด้วยสิ่งนี้ ไฟล์สามารถสื่อสารข้อมูลเมตา XMP ไปยังภาพยนตร์ SWF ผ่าน ActionScript
- **กล่อง ilst**: กล่องนี้เกิดขึ้นภายในกล่อง Meta (เมตา) และสามารถมีแท็กข้อมูลเมตาจำนวนหนึ่ง ประเภทข้อมูลที่สนับสนุนได้รับด้านล่าง
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **กล่อง Text Track Metadata**: ตัวอย่างข้อความ (text หรือ tx3g) ภายใน Media Databox (mdat) สามารถประกอบด้วยกล่องข้อมูลเมตาต่อไปนี้
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## อ้างอิง ##

- [แฟลชวิดีโอ - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

