---
date: 2022-03-20
keywords: mxl, פורמט קובץ Musepack, סיומת .mxl
מְחַבֵּר:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "למד על פורמט קובץ MXL וממשקי API שיכולים ליצור ולפתוח קבצי MXL."
title: פורמט קובץ MXL - קובץ MusicXML דחוס
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## מהו קובץ MXL?

קובץ MXL הוא הצורה הדחוסה של פורמט קובץ MusicXML שהוא פורמט סטנדרטי פתוח להחלפת תווים דיגיטליים. קבצי MusicXML בטקסט רגיל הם גדולים בגודלם והשימוש בקבצים כאלה כפורמט הפצת גיליונות הושפע מגודל הקובץ הגדול. בעיה זו טופלה עם [MusicXML](https://www.musicxml.com/) 2.0 על ידי הצגת פורמט הקובץ MXL שדוחס את הקבצים מספיק כדי להקטין את גודל הקובץ בדומה לזה של קבצי MIDI מקוריים. סוג המדיה המומלץ עבור קובצי MXL הוא application/vnd.recordare.musicxml.

## פורמט קובץ MXL

קבצי MXL מאוחסנים כקבצי [ZIP](/he/compression/zip/) דחוסים [XML](/he/web/xml/) עם סיומת קובץ .mxl. קבצי MXL נדחסים עם אלגוריתם DEFLATE כפי שצוין ב-[RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### מבנה קובץ MXL

לכל קובץ MXL יש פורמט XML מבוסס ZIP שחייב להיות בעל קובץ META-INF/container.xml שמתאר את נקודת ההתחלה של גרסת MusicXML של הקובץ. לא הוגדר קובץ ‎.xsd מתאים עבור פורמט הקובץ MXL.

לקובץ container.xml פשוט יש את התוכן כדלקמן. דוגמה זו נלקחה מקובץ Dichterliebe01.mxl הזמין באתר MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
בדוגמה זו, ה<container> אלמנט הוא רכיב המסמך. ה<rootfiles> אלמנט יכול להכיל אחד או יותר<rootfile> אלמנטים, עם הראשון<rootfile> רכיב המתאר את שורש MusicXML. קובץ MusicXML המשמש בתור א<rootfile> ייתכן שיש לי<score-partwise> ,<score-timewise> , או<opus> כרכיב המסמך שלו.

## הפניות

* [קבצי MXL דחוסים](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

