---
date: 2019-10-11
keywords: prc, .prc, פורמט קובץ prc, כיצד לפתוח קבצי prc, סיומת .prc, סיומת prc
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: פורמט קובץ PRC
linktitle: PRC
description: "למד על פורמט קובץ PRC וממשקי API שיכולים ליצור ולפתוח קבצי PRC."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## פורמטים של קובץ PRC
הסיומות ".prc" משמשות עבור פורמט קובץ תלת מימד קומפקטי של ייצוג מוצר ופורמט קובץ של ספר אלקטרוני על ידי MobiPocket.

## מהו קובץ ייצוג מוצר (PRC)?

PRC (Product Representation Compact) הוא פורמט קובץ תלת מימדי המותאם לאחסון, טעינה והצגה של נתונים תלת מימדיים במיוחד המגיעים ממערכות CAD (עיצוב בעזרת מחשב). זהו קובץ בינארי רציף, כתוב בצורה ניידת. ניתן להשתמש ב-PRC כדי להטמיע נתונים תלת מימדיים בקובץ PDF. PRC תומך ברוב המבנים העיקריים של CAD כגון מכלולים וחלקים, עצים של ישויות תלת-ממדיות, ייצוג גיאומטריה מדויקת, ייצוג משולש וסימון. PRC משתמש בסיומת .prc וסוג המדיה האינטרנטית בשימוש הוא *model/prc*.

PRC הוא פורמט קובץ רב-תכליתי אשר על סמך השימוש בו ניתן לאחסן באמצעות דחיסה רגילה לייצוג ישיר של נתוני CAD או להיות מאוחסן באמצעות דחיסה גבוהה כדי להקטין את גודל הקובץ. הנתונים התלת-ממדיים המאוחסנים ב-PDF בפורמט PRC ניתנים להפעלה הדדית עם יישומי CAM ו-CAE.

### מפרט פורמט קובץ של ייצוג מוצר קומפקטי (PRC).

לקובץ PRC יש קטע כותרת ראשי אחד ואחריו מבני קובץ אחד או יותר ואחריו קובץ דגם אחד בסוף. למבנה קובץ יש כותרת אחת ואחריה קטעי הנתונים הבאים:

- **גלובלים**: הוא מכיל את מבני הקבצים והצבעים אליהם מתייחסים, סגנונות הקו ומערכות הקואורדינטות עבור כל ישות עץ במבנה הקובץ.
- **עץ**: הוא מכיל תיאור של עץ הפריטים כמו מופעי מוצרים, הגדרות חלקים, פריטי ייצוג וסימון.
- **Tessellation**: הוא מכיל את כל הנתונים המשולשים (משולשים) בישויות העלים של העץ (פריטי ייצוג וסימון).
- **גיאומטריה**: הוא מכיל את כל נתוני הגיאומטריה והטופולוגיה המדויקים של ישויות העלים של העץ (פריטי ייצוג).
- **גיאומטריה נוספת**: היא מכילה את נתוני הסיכום של הגיאומטריה. זה מאפשר לטעון חלקית את הקובץ מבלי לטעון את כל הגיאומטריה.

להלן המבנה של קובץ PRC טיפוסי.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## מהו קובץ ספר אלקטרוני של MobiPocket עם סיומת PRC
פורמט קובץ ספר אלקטרוני שהוצג על ידי חברה צרפתית בשם **Mobipocket** משתמש גם בסיומת ".prc". בתחילה, Mobipocket השיקה אפליקציה חינמית למספר מכשירים חכמים כמו מחשבי טאבלט, מחשבי כף יד וסמארטפונים. סיומת ".prc" זהה למעשה ל-.mobi אך משמשת במיוחד עבור מחשבי כף יד אשר תומכים רק בהרחבות **.prc** או **.pdb**.

### מפרטי פורמט קובץ Mobipocket PRC
פורמט הקובץ MobiPocket PRC מבוסס על תקן Open eBook באמצעות XHTML והוא גם יכול לכלול JavaScript ומסגרות. זמינה גם תמיכה בשאילתות SQL מקוריות לשימוש עם מסדי נתונים משובצים.

ל-Mobipocket Reader יש ספריית דפי בית. הקוראים יכולים להוסיף דפים ריקים בכל חלק של הספר ולהוסיף ציורים משתנים. האובייקטים כמו הערות, סימניות, תיקונים, הערות וציורים ניתנים לניהול ממיקום אחד. תמונות מומרות לפורמט GIF ובעלות גודל מקסימלי של 64K שמספיק לטלפונים ניידים עם מסכים קטנים. Mobipocket Reader כולל את הסימניות האלקטרוניות ומילון מובנה.

לקורא מצב מסך מלא לקריאה ותמיכה עבור מחשבי כף יד, תקשורת וסמארטפונים רבים. מוצרי Mobipocket תומכים ברוב מערכות ההפעלה של Palm, Windows, Symbian, BlackBerry, אך לא באנדרואיד. הקורא עובד תחת Linux או Mac OS X באמצעות WINE.

## הפניות

- [PRC - ויקיפדיה](https://en.wikipedia.org/wiki/PRC_(file_format))
- [מפרט פורמט PRC](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [השוואה של פורמטים של ספרים אלקטרוניים - מאת ויקיפדיה](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

