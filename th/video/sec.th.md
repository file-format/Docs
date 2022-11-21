---
date: 2022-03-25
keywords: วินาที, .sec, รูปแบบไฟล์ sec, รูปแบบไฟล์ .sec, นามสกุล .sec, นามสกุล sec,
ผู้เขียน:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ SEC และ API ที่สามารถสร้างและเปิดไฟล์ SEC"
title: รูปแบบไฟล์ SEC - ไฟล์วิดีโอความปลอดภัยของ Samsung,
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## ไฟล์ SEC คืออะไร??

ไฟล์ SEC เป็นไฟล์วิดีโอที่สร้างขึ้นด้วยระบบเฝ้าระวัง Samsung DVR วิดีโอถูกจับจากกล้องวงจรปิดและจัดเก็บไว้ในแผ่นดิสก์ในรูปแบบ SEC สามารถเล่นวิดีโอ SEC ที่บันทึกไว้ได้ด้วยซอฟต์แวร์วิดีโอของ Samsung ที่สามารถจัดการฟีดวิดีโอจากกล้องหลายตัว

## รูปแบบไฟล์ SEC - ข้อมูลเพิ่มเติม

ไฟล์ SEC มีสตรีม h264/AVC ภายในโดยใช้รูปแบบไฟล์ที่เป็นกรรมสิทธิ์ ส่วนหัวของไฟล์ SEC เริ่มต้นด้วยหมายเลขรุ่นของ SRD-1670D ข้อมูลวันที่และเวลาจะอยู่ที่ส่วนท้ายของไฟล์

### แปลงไฟล์ SEC เป็น AVI

ไฟล์ SEC สามารถแปลงเป็นรูปแบบไฟล์มาตรฐาน [AVI](/th/video/avi/) โดยใช้ FFmpeg

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## อ้างอิง ##

- [ไฟล์ Samsung และ SEC](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

