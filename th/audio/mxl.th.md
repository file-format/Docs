---
date: 2022-03-20
keywords: mxl, รูปแบบไฟล์ Musepack, นามสกุล .mxl,
ผู้เขียน:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ MXL และ API ที่สามารถสร้างและเปิดไฟล์ MXL"
title: รูปแบบไฟล์ MXL - ไฟล์ MusicXML ที่บีบอัด,
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## ไฟล์ MXL คืออะไร??

ไฟล์ MXL เป็นรูปแบบการบีบอัดของรูปแบบไฟล์ MusicXML ซึ่งเป็นรูปแบบมาตรฐานเปิดสำหรับการแลกเปลี่ยนแผ่นเพลงดิจิทัล ไฟล์ MusicXML แบบข้อความล้วนมีขนาดใหญ่ และการใช้ไฟล์ดังกล่าวในรูปแบบการแจกจ่ายแผ่นงานได้รับผลกระทบจากขนาดไฟล์ที่ใหญ่ ปัญหานี้ได้รับการแก้ไขด้วย [MusicXML](https://www.musicxml.com/) 2.0 โดยแนะนำรูปแบบไฟล์ MXL ที่บีบอัดไฟล์มากพอที่จะลดขนาดไฟล์ให้ใกล้เคียงกับขนาดไฟล์ MIDI ดั้งเดิม ประเภทสื่อที่แนะนำสำหรับไฟล์ MXL คือ application/vnd.recordare.musicxml

## รูปแบบไฟล์ MXL

ไฟล์ MXL จัดเก็บเป็นไฟล์ [ZIP](/th/compression/zip/) บีบอัด [XML](/th/web/xml/) ที่มีนามสกุลไฟล์ .mxl ไฟล์ MXL ถูกบีบอัดด้วยอัลกอริธึม DEFLATE ตามที่ระบุไว้ใน [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

### โครงสร้างไฟล์ MXL

ไฟล์ MXL แต่ละไฟล์มีรูปแบบ XML ที่ใช้ ZIP ซึ่งต้องมีไฟล์ META-INF/container.xml ซึ่งอธิบายจุดเริ่มต้นของไฟล์เวอร์ชัน MusicXML ไม่มีไฟล์ .xsd ที่กำหนดไว้สำหรับรูปแบบไฟล์ MXL

ไฟล์ container.xml อย่างง่ายมีเนื้อหาดังนี้ ตัวอย่างนี้นำมาจากไฟล์ Dichterliebe01.mxl ที่มีอยู่ในเว็บไซต์ MakeMusic

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
ในตัวอย่างนี้<container> องค์ประกอบคือองค์ประกอบของเอกสาร เดอะ<rootfiles> องค์ประกอบสามารถมีตั้งแต่หนึ่งรายการขึ้นไป<rootfile> องค์ประกอบด้วยประการแรก<rootfile> องค์ประกอบที่อธิบายราก MusicXML ไฟล์ MusicXML ที่ใช้เป็นไฟล์<rootfile> อาจจะมี<score-partwise> ,<score-timewise> , หรือ<opus> เป็นองค์ประกอบเอกสาร

## อ้างอิง

* [ไฟล์ MXL บีบอัด](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

