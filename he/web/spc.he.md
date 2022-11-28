---
date: 2021-07-05
keywords: spc, .spc, פורמט קובץ spc, כיצד לפתוח קבצי spc, קובץ אישורי מפרסם תוכנה
מְחַבֵּר:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - Software Publisher Certificate File
linktitle: SPC
description: "למד על פורמט קובץ SPC וממשקי API שיכולים ליצור ולפתוח קובצי SPC."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## מהו קובץ SPC?

קובץ עם סיומת .spc הוא קובץ אישור אבטחה דיגיטלי שנוצר בפורמט PKCS #7. מספר יישומים, יוצרים קבצי אישורים אלה להחלפה מאובטחת של מידע. מעט יישומים כאלה כוללים את OpenSSL ואת היישום Signcode.exe הכלול ב-.NET Framework של מיקרוסופט. כמו קובצי אישור אחרים כגון [.cer](/he/web/cer/), [.p7c](/he/web/p7c/) ו-[.ssp](/he/web/ssp/), קובצי ה-SPC מכילים את המפתח הציבורי מידע מוצפן עם מפתח פרטי. ניתן לשתף מפתח ציבורי זה עם משתמשים באופן ציבורי בעוד המפתח הפרטי נשמר בסודיות.

## פורמט קובץ SPC - מידע נוסף

קבצי ה-SPC נשמרים בדיסק כקבצים בינאריים שניתן לפתוח בכל עורך טקסט אך אינם ניתנים לקריאה אנושית. אלה מבוססים על הגרסה העדכנית ביותר של PKCS # 7 הזמינה [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## הפניות

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [Reference SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

