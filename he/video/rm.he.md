---
date: 2019-10-11
keywords: rm, .rm, פורמט קובץ rm, פורמט קובץ .rm, סיומת .rm, פורמט קובץ RealMedia
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "למד על פורמט קבצי RM וממשקי API שיכולים ליצור ולפתוח קבצי RM."
title: פורמט קובץ RM
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## מהו קובץ RM? ##

RealMedia הוא פורמט מיכל קנייני של מולטימדיה שפותח על ידי RealNetworks המשתמש בסיומת rm. הוא משמש עם השילוב של [RealAudio (RA)](/he/audio/ra/) ו-[RealVideo(RV)](/he/video/rv/) לסטרימינג דרך האינטרנט. זרמים אלה הם בקצב סיביות קבוע. עבור קצב סיביות משתנה, RealNetworks פיתחה את פורמט RealMedia Variable Bitrate (RMVB). RealMedia מתאימה להזרמת תוכן דרך האינטרנט וניתן להשתמש בה למשל להזרמת טלוויזיה בשידור חי.

## מבנה של קובץ RealMedia ##

קובץ RealMedia מורכב מסדרה של נתחים, שלכל אחד מהם המבנה הבא:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

להלן סוגי הנתחים הקיימים בקובץ RealMedia:

- **כותרת קובץ RealMedia (.RMF)**: זה חייב להיות הנתח הראשון בקובץ RealMedia. רק נתח RMF אחד קיים בקובץ אחד. הוא מכיל מידע על מספר הכותרות.
- **כותרת מאפייני קובץ (PROP)**: זו מכילה מידע על המאפיינים הכלליים של קובץ RealMedia. יש רק נתח אחד מסוג זה בכל קובץ RealMedia.
- **כותרת מאפייני מדיה (MDPR)**: נתח זה מכיל מידע על מאפייני הזרם. הוא מכיל מידע על סוג הזרם וה-Codec בשימוש. יש נתח MDPR אחד לכל זרם בקובץ.
- **כותרת תיאור התוכן (CONT)**: חלק זה מכיל מידע טקסט כמו הכותרת או המחבר של התוכן בקובץ RealMedia. נתח זה מיועד למטרות מידע בלבד.
- **כותרת נתונים (DATA)**: נתח זה מכיל קבוצה של מנות נתונים.
- **כותרת אינדקס (INDX)**: נתח זה מגיע אחרי כל נתחי ה-DATA ומכיל ערכי אינדקס. קובץ אחד יכול לכלול יותר מנתחי INDX אחד.

## פורמטי אודיו ווידאו נתמכים ##

### פורמטי שמע ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: Sipro
- לבשל: לבשל
- atrc: ATRAC3
- ralf: RealAudio Lossless Format
- raac: LC-AAC
- racp: HE-AAC

### פורמטים של וידאו ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: מבשר H.264
- RV40: מבשר H.264, RV40
- RVTR: H.263+ (RV20)

## הפניות ##

- [RealMedia - ויקיפדיה](https://en.wikipedia.org/wiki/RealMedia)

