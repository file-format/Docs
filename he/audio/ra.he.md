---
date: 2019-12-13
keywords: ra, פורמט קובץ ra, סיומת .ra, פורמט קובץ אודיו אמיתי, פורמט אודיו ra, פורמט קובץ RealAudio
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "למד על פורמט קבצי RA וממשקי API שיכולים ליצור ולפתוח קבצי RA."
title: פורמט קובץ RA
linktitle: RA
menu:
  docs:
    parent: "audio"
lastmod: 2020-28-12
---

## מהו קובץ RA?

RealAudio (RA) הוא פורמט אודיו קנייני שפותח על ידי Real Networks, Inc. ושוחרר באפריל 1995. הוא משתמש בסיומת ra עבור הקבצים שלו. הוא משתמש ב-bitrate נמוך כמו גם ב-codec שמע נאמנות גבוהה. RA שימש להזרמת אודיו דרך האינטרנט על ידי תחנות רדיו רבות באינטרנט. אתר ה-BBC השתמש בכבדות ב-RA עד 2009, אך הופסק במרץ 2011.

## הרחבת קובץ מאת RealNetworks ##

RealNetworks השתמשה בפורמט קובץ RA עבור שמע. RealNetworks החלה להציע פורמט וידאו ([RealVideo](/he/video/rv/)) בשנת 1997 עם סיומת rv. [RealMedia (RM)](/he/video/rm/) שימש לשילוב של פורמטים של אודיו ווידאו. עם המהדורה האחרונה של RealProduce (המקודד של Real), נעשה שימוש בפורמט RV עבור קובצי וידאו ופורמט [RealMedia Variable Bitrate (RMVB)](/he/video/rmvb/) משמש לקובצי וידאו VBR (Variable bitrate).

## הזרמת אודיו ##

RA פותח כפורמט מדיה זורמת וניתן להזרים אותו באמצעות HTTP. קובץ האודיו מתחיל להתנגן ברגע שהחלק הראשון של הקובץ מתקבל וממשיך להתנגן עם הורדת שאר הקובץ.

הגרסה הראשונה של RealAudio השתמשה בפרוטוקול PNA או PNM הקנייני כדי להזרים אודיו. מאוחר יותר הם עברו ל-RTSP סטנדרטי של IETF (Real Time Streaming Protocol) לניהול חיבורים. כדי לשלוח נתונים, הם השתמשו בפרוטוקול RDT (Real Data Transfer). הפרוטוקול נשמר בסוד בתחילה, אך מאוחר יותר חלק ממנו התפרסם באמצעות פרויקט Helix.

כדי להזרים קבצי RealAudio, רוב הדפים מקשרים לקובץ RAM (Real Audio Metadata) או SMIL (Synchronized Multimedia Integration Language). קובץ זה משמש לטעינת נגן המדיה של המשתמש ולהזרים את האודיו מכתובת האתר הכלולה בקובץ.

## RealAudio Audio Codec ##

להלן רשימה של רכיבי קוד אודיו המזוהים כל אחד באמצעות קוד בן ארבעה תווים יחד עם הגרסה של RealAudio שהציגה אותו.

|Codec|גרסת RealAudio|
|---|---|
|lpcJ ו-14_4|1|
|28_8|2|
|dnet|3|
|sipr|4/5|
|לבשל|6|
|atrc|8|
|raac|9|
|racp|10|
|ralf|10|

## הפניות ##

- [RealAudio - ויקיפדיה](https://en.wikipedia.org/wiki/RealAudio)

