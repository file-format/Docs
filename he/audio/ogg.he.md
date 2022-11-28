---
date: 2019-12-13
keywords: ogg, פורמט קובץ ogg, סיומת .ogg, פורמט שמע ogg
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "למד על פורמט קובץ OGG וממשקי API שיכולים ליצור ולפתוח קובצי OGG."
title: קובץ OGG - קובץ אודיו של Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## מהו קובץ OGG?

OGG הוא קובץ אודיו דחוס של Ogg Vorbis שנשמר עם סיומת .ogg. קבצי OGG משמשים לאחסון נתוני אודיו ויכולים לכלול מידע על אמן ורצועה ומטא נתונים. OGG הוא פורמט מיכל חינמי ופתוח שמתוחזק על ידי Xiph.Org Foundation.

## היסטוריה קצרה של פורמט קובץ OGG

פרויקט Ogg החל כחלק מפרויקט גדול יותר בשנת 1993 ונקרא Squish אך בגלל סימן מסחרי קיים, שונה שמו ל- OggSquish. זה תואר כניסיון ליצור פורמט אודיו דחוס גמיש עבור יישומי אודיו מודרניים. התייחסות OGG הופרדה מ- Vorbis ב-2 בספטמבר 2000.

OGM נוצר בשנת 2002 עקב היעדר תמיכת וידאו רשמית ב- OGG. זה אפשר להטמיע וידאו ממסגרת Microsoft DirectShow לתוך עטיפה מבוססת OGG. עד 2006, OGG נתמך על ידי מנועי משחקי וידאו רבים והיה בשימוש נפוץ לקידוד תוכן חינמי. קרן התוכנה החופשית החלה בקמפיין ב-15 במאי 2007, להגברת השימוש ב-Vorbis כחלופה מעולה ל-MP3. עד 30 ביוני 2009, OGG היה פורמט המכולה היחיד שנתמך על ידי יישום HTML5 של Firefox 3.5.

## פורמט קובץ OGG

פורמט OGG מורכב מגושים של נתונים. כל נתח נקרא דף Ogg. כל עמוד מתחיל ב-"OggS" כדי לזהות את פורמט Ogg. הכותרת מכילה את המספר הסידורי ומספר העמוד המזהים כל עמוד כחלק מסדרה. העמוד מורכב מהרכיבים הבאים.

- **ראש הדף**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| קצת | ערך | תיאור |
| --- | --- | --- |
| 0 | 0x01 | מציין שהחבילה הראשונה של העמוד היא המשכה של החבילה הקודמת בזרם הסיביות הלוגי. |
| 1 | 0x02 | מציין שדף זה הוא הראשון בזרם הסיביות הלוגי. |
| 2 | 0x04 | מציין שדף זה הוא האחרון בזרם הסיביות הלוגי. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **מטא נתונים**: VorbisComment הוא המנגנון הנתמך ביותר לאחסון מטא נתונים. מנגנונים אחרים כוללים את הדברים הבאים:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## הפניות ##

- [OGG - ויקיפדיה](https://en.wikipedia.org/wiki/Ogg)

