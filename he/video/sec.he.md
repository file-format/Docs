---
date: 2022-03-25
keywords: sec, .sec, פורמט קובץ sec, פורמט קובץ .sec, סיומת .sec, סיומת sec
מְחַבֵּר:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "למד על פורמט קובץ SEC וממשקי API שיכולים ליצור ולפתוח קובצי SEC."
title: פורמט קובץ SEC - קובץ וידאו אבטחה של סמסונג
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## מהו קובץ SEC?

קובץ SEC הוא קובץ וידאו שנוצר עם מערכת המעקב של Samsung DVR. וידאו נקלט ממצלמות מעקב ומאוחסן על דיסק בפורמט SEC. ניתן להפעיל את סרטון ה-SEC המוקלט עם תוכנת הווידאו של סמסונג שיכולה לנהל הזנת וידאו ממספר מצלמות.

## פורמט קובץ SEC - מידע נוסף

קבצי SEC מכילים זרם h264/AVC בפנים באמצעות פורמט קובץ קנייני. הכותרת של קובץ SEC מתחילה במספר הדגם של SRD-1670D. פרטי התאריך והשעה נשמרים בסוף הקובץ.

### המרת קובץ SEC ל-AVI

ניתן להמיר קובץ SEC לפורמט הקובץ הסטנדרטי [AVI](/he/video/avi/) באמצעות FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## הפניות ##

- [קבצי סמסונג ו-SEC](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

