---
date: 2022-05-09
מְחַבֵּר:
  display_name: Kashif Iqbal
draft: false
toc: true
title: פורמט קובץ PYD - Python Dynamic Module
linktitle: PYD
description: "למד על פורמט קובץ PYD וממשקי API שיכולים ליצור ולפתוח קובצי PYD."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## מהו קובץ PYD?

קובץ PYD הוא ספריית קישורים דינמית שנכתבה ב-Python שניתן להפעיל על ידי קוד אחר של Python בזמן הריצה. הוא מכיל מודול Python אחד או יותר המאפשר שימוש חוזר בקוד ומספק ארכיטקטורת מודול לכתיבת יישומים. ניתן ליצור ולשמור קובצי PYD עם סיומת pyd למשל helloworld.pyd. מפתחי יישומים יכולים להשתמש בהצהרת ייבוא כדי לכלול את מודולי ה-PYD באפליקציות שלהם. ניתן לפתוח קובצי PYD עם Python Software Foundation Python שזמין עבור מערכת ההפעלה Windows, Mac ו-Linux.

## פורמט קובץ PYD - מידע נוסף

קובצי PYD נכתבים בשפת התכנות Python ומופקים על ידי קומפילציה של קוד Python.

## ההבדל בין תבניות קובץ PY ו-PYD

קובץ [PY](/he/programming/py/) מכיל קוד מקור שמופעל כפי שהוא ואינו יכול להיכלל כקוד לשימוש חוזר ביישומי Python אחרים. עם זאת, קובץ PYD הוא ספרייה מקושרת דינמית לשימוש במערכת ההפעלה Windows.

## כיצד ליצור קובץ PYD?

ניתן ליצור קובץ PYD על ידי יצירת מודול עם שם למשל exmaple.pyd. מודול זה יכיל את כל הפונקציונליות בצורה של פונקציה אחת או יותר, למשל PyMod_example(). כאשר התוכנית כוללת את הספרייה הזו וקוראת לה, ניתן לעשות זאת על ידי ייבוא המודול והפונקציה PyMod_example() תפעל.

## הפניות ##

* [יצירת הרחבות Python ב-C/C++](https://sebsauvage.net/python/mingw.html)
* [Python (שפת תכנות) - ויקיפדיה](https://en.wikipedia.org/wiki/Python_(programming_language))

