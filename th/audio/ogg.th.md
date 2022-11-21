---
date: 2019-12-13
keywords: ogg, รูปแบบไฟล์ ogg, นามสกุล .ogg, รูปแบบเสียง ogg,
ผู้เขียน:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ OGG และ API ที่สามารถสร้างและเปิดไฟล์ OGG"
title: ไฟล์ OGG - ไฟล์เสียง Ogg Vorbis,
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## ไฟล์ OGG คืออะไร??

OGG เป็นไฟล์เสียงบีบอัด Ogg Vorbis ที่บันทึกด้วยนามสกุล .ogg ไฟล์ OGG ใช้สำหรับจัดเก็บข้อมูลเสียงและสามารถรวมศิลปินและข้อมูลแทร็กและข้อมูลเมตาได้เช่นกัน OGG เป็นรูปแบบคอนเทนเนอร์แบบเปิดและฟรีที่ดูแลโดย Xiph.Org Foundation

## ประวัติโดยย่อของรูปแบบไฟล์ OGG

โครงการ Ogg เริ่มต้นโดยเป็นส่วนหนึ่งของโครงการขนาดใหญ่ในปี 1993 และมีชื่อว่า Squish แต่เนื่องจากมีเครื่องหมายการค้าอยู่แล้ว จึงเปลี่ยนชื่อเป็น OggSquish มีการอธิบายว่าเป็นความพยายามในการสร้างรูปแบบเสียงที่บีบอัดอย่างยืดหยุ่นสำหรับแอปพลิเคชันเสียงสมัยใหม่ การอ้างอิง OGG ถูกแยกออกจาก Vorbis เมื่อวันที่ 2 กันยายน พ.ศ. 2543

OGM ก่อตั้งขึ้นในปี 2545 เนื่องจากขาดการสนับสนุนวิดีโออย่างเป็นทางการใน OGG สิ่งนี้อนุญาตให้ฝังวิดีโอจาก Microsoft DirectShow framework ลงใน wrapper ที่ใช้ OGG ภายในปี 2549 OGG ได้รับการสนับสนุนโดยเอ็นจิ้นวิดีโอเกมจำนวนมากและมักใช้ในการเข้ารหัสเนื้อหาฟรี มูลนิธิซอฟต์แวร์เสรีเริ่มรณรงค์เมื่อวันที่ 15 พฤษภาคม พ.ศ. 2550 เพื่อเพิ่มการใช้ Vorbis เป็นทางเลือกที่เหนือกว่า MP3 ภายในวันที่ 30 มิถุนายน พ.ศ. 2552 OGG เป็นรูปแบบคอนเทนเนอร์เดียวที่สนับสนุนโดยการใช้ HTML5 ของ Firefox 3.5

## รูปแบบไฟล์ OGG

รูปแบบ OGG ประกอบด้วยข้อมูลจำนวนมาก แต่ละอันเรียกว่าหน้า Ogg แต่ละหน้าขึ้นต้นด้วย "OggS" เพื่อระบุรูปแบบ Ogg ส่วนหัวประกอบด้วยหมายเลขซีเรียลและหมายเลขหน้าที่ระบุแต่ละหน้าเป็นส่วนหนึ่งของชุดข้อมูล หน้าประกอบด้วยส่วนประกอบต่อไปนี้

- **ส่วนหัวของหน้า**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| บิต | ค่า | คำอธิบาย |
| --- | --- | --- |
| 0 | 0x01 | ระบุว่าแพ็กเก็ตแรกของเพจคือความต่อเนื่องของแพ็กเก็ตก่อนหน้าในลอจิคัลบิตสตรีม |
| 1 | 0x02 | ระบุว่าหน้านี้เป็นหน้าแรกในบิตสตรีมแบบลอจิคัล |
| 2 | 0x04 | ระบุว่าหน้านี้เป็นหน้าสุดท้ายในลอจิคัลบิตสตรีม |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **ข้อมูลเมตา**: VorbisComment เป็นกลไกที่ได้รับการสนับสนุนอย่างกว้างขวางที่สุดสำหรับการจัดเก็บข้อมูลเมตา กลไกอื่นๆ ได้แก่:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## อ้างอิง ##

- [OGG - วิกิพีเดีย](https://en.wikipedia.org/wiki/Ogg)

