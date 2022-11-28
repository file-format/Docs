---
date: 2022-01-06
keywords: vtt, .vtt, פורמט קובץ vtt, פורמט קובץ .vtt, סיומת .vtt, סיומת vtt
מְחַבֵּר:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "למד על קבצי ‎.vtt וממשקי API שיכולים ליצור ולפתוח קובצי VTT."
title: פורמט קובץ VTT - קובץ רצועות טקסט וידאו באינטרנט
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## מהו קובץ VTT?

קובץ VTT הוא קובץ טקסט המכיל מידע להצגת רצועות טקסט מתוזמנות (כגון כתוביות או כיתובים) בפורמט Web Video Text Tracks (WebVTT). רצועות הטקסט המתוזמנות כוללות מידע כגון כתוביות או כיתובים. מטרת קובץ VTT היא להוסיף שכבות טקסט ל-a<video> . הפורמט דומה במקצת לקבצי SRT. קובצי טקסט מבוססי WebVTT מקודדים באמצעות UTF-8. קובץ VTT מכיל מידע כגון כתוביות, תיאורים, כיתובים, תיאורים, פרקים ומטא נתונים. בהיותם קבצי טקסט רגילים, ניתן לפתוח קובצי VTT באמצעות עורכי טקסט כגון Microsoft Notepad, Apple TextEdit ו-Notepad++.

## פורמט קובץ VTT - מידע נוסף

קובצי VTT משתמשים בפורמט הקובץ WebVTT לשמירת מידע על רצועות טקסט עוקבות. כל רצועת טקסט מתוזמן מורכבת משורה בודדת או שורות מרובות, המכונה גם 'רמז' כפי שמוצג בדוגמה הבאה.

### דוגמה לקובץ VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### מבנה קובץ VTT

להלן דרישות המבנה של קובץ VTT.

* סימן סדר בתים אופציונלי (BOM).
* המחרוזת "WEBVTT".
* כותרת טקסט אופציונלית מימין ל-WEBVTT.
* שורה ריקה, המקבילה לשתי שורות חדשות עוקבות.
* אפס או יותר רמזים או הערות.
* אפס שורות ריקות או יותר.

## הפניות

* [VTT - W3 בתי ספר](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

