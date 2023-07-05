---
date: 2022-03-25
keywords: sec , sec , تنسيق ملف sec , تنسيق ملف .sec , ملحق. sec , ملحق sec
مؤلف:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "تعرف على تنسيق ملف SEC و APIs التي يمكنها إنشاء ملفات SEC وفتحها."
title: تنسيق ملف SEC - ملف فيديو أمان Samsung
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## ما هو ملف SEC؟

ملف SEC هو ملف فيديو تم إنشاؤه باستخدام نظام مراقبة Samsung DVR. يتم التقاط الفيديو من كاميرات المراقبة وتخزينه على قرص بتنسيق SEC. يمكن تشغيل فيديو SEC المسجل باستخدام برنامج فيديو سامسونج الذي يمكنه إدارة تدفق الفيديو من عدة كاميرات.

## تنسيق ملف SEC - مزيد من المعلومات

تحتوي ملفات SEC على دفق h264 / AVC بالداخل باستخدام تنسيق ملف خاص. يبدأ رأس ملف SEC برقم طراز SRD-1670D. يتم الاحتفاظ بمعلومات التاريخ والوقت في نهاية الملف.

### تحويل ملف SEC إلى AVI

يمكن تحويل ملف SEC إلى تنسيق الملف القياسي [AVI](/ar/video/avi/) باستخدام FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## مراجع ##

- [ملفات Samsung و SEC](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

