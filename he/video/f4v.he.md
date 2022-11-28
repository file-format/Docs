---
date: 2019-10-11
keywords: פורמט קובץ f4v, .f4v, f4v, פורמט קובץ .f4v, סיומת .f4v, סיומת f4v, פורמט וידאו f4v, כיצד לפתוח קבצי f4v, מהם קבצי f4v
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "למד על פורמט קובץ F4V וממשקי API שיכולים ליצור ולפתוח קבצי F4V"
title: פורמט קובץ F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## מהו קובץ F4V? ##

F4V (קובץ וידאו פלאש MP4) הוא קובץ וידאו שנשמר עם סיומת .f4v. הוא מבוסס על פורמט קובץ המדיה הבסיסי של ISO (MPEG-4 חלק 12). זה דומה מאוד ל-[MP4](/he/video/mp4/) וזו הסיבה שהוא מכונה גם Flash MP4 באופן לא פורמלי. ל-[FLV](/he/video/flv/) היו מגבלות בעת הזרמת תוכן H.264/ACC, מה שהביא לכך ש-Adobe Systems יצרה את הפורמט החדש F4V. Flash Player יכול לנגן קבצי F4V מאז שחרורו של Flash Player 9 Update 3.

## מבנה של קבצי F4V ##

פורמט הקובץ F4V מבוסס על פורמט קובץ המדיה הבסיסי ISO (MPEG-4 Part 12) והוא דומה מאוד לפורמט MP4. לפרטים לגבי המבנה, עיין בדף [MP4](/he/video/mp4/). ההבדל העיקרי בין F4V ל-MP4 הוא פורמטי המטא נתונים ש-F4V יכול לאחסן. להלן רשימת פורמטי המטא נתונים הנתמכים על ידי פורמט F4V.

- **תיבת תגים**: ארבע תיבות תג אופציונליות נוספות (auth, title, dscp, cprt) בתוך תיבת הסרט (moov).
- **תיבת XMP Metadata**: תיבה זו מגיעה מיד אחרי תיבת הסרט (moov). בעזרת זה, הקובץ יכול להעביר מטא נתונים של XMP לסרט SWF באמצעות ActionScript.
- **תיבה בתיבה**: תיבה זו מופיעה בתוך תיבת המטא (מטה) ויכולה להכיל מספר תגיות מטא נתונים. סוגי הנתונים הנתמכים ניתנים להלן.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **תיבת Metadata של רצועת טקסט**: דוגמאות הטקסט (טקסט או tx3g) בתוך תיבת המדיה (mdat). זה יכול להכיל את תיבות המטא נתונים הבאות.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## הפניות ##

- [וידאו פלאש - ויקיפדיה](https://en.wikipedia.org/wiki/Flash_Video)

