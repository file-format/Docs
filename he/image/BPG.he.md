---
date: 2020-08-12
keywords: bpg, .bpg, פורמט קובץ bpg, כיצד לפתוח קבצי bpg, סיומת .bpg, סיומת bpg
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: פורמט קובץ BPG
linktitle: BPG
description: "למד על פורמט קבצי BPG וממשקי API שיכולים ליצור ולפתוח קובצי BPG."
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## מהו קובץ BPG? ##

BPG (Better Portable Graphics) הוא פורמט קובץ שנוצר על ידי Fabrice Bellard בשנת 2014 עבור תמונות דיגיטליות. הוא הציע BPG כתחליף ל-JPEG מכיוון ש-BPG היה יעיל יותר בדחיסה או בגודל. BPG משתמש בקידוד תוך-פריים של תקן דחיסת וידאו HEVC (High-Efficiency Video Coding).

BPG תוכנן כפורמט נייד יעיל בזיכרון לעבודה על מכשירי כף יד ו-IoT. נכון לעכשיו, דפדפני אינטרנט אינם תומכים בפורמט BPG, אך אתרים עדיין יכולים לספק תמונות BPG באמצעות ספריית JavaScript שנכתבה על ידי Bellard. BPG משתמש בפרופיל הראשי של 4:4:4 16 תמונת סטילס של HEVC עד 14 ביטים לדגימה.

## מפרטים ##

פורמט מיכל BPG הוא פורמט תמונה גנרי ולא זרם הסיביות הגולמי המשמש ב-HEVC. BPG תומך בפורמטים של צבע 4:4:4, 4:2:2 ו-4:2:0. ערוץ אלפא נתמך גם עם ערוץ נוסף מקודד בנפרד או הערוץ הרביעי של תמונת CMYK. BPG מספקת תמיכה במטא נתונים עבור Exif, פרופילי ICC ו-XMP. BPG תומך ב-YCbCr (ITU-R BT.601, BT.709 ו-BT.2020 (זוהר לא קבוע)), YCgCo, RGB, CMYK ומרחב צבע בגווני אפור. BGP תומך גם באנימציה ובדחיסת נתונים HEVC חסרי אובדן וחסר אובדן.

## הפניות ##

- [Better Portable Graphics - ויקיפדיה](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

