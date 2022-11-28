---
date: 2021-07-05
keywords: פורמט קובץ ssp, .ssp, ssp, כיצד לפתוח קבצי ssp, Scala Server Page
מְחַבֵּר:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - פורמט קובץ Scala Server Pages
linktitle: SSP
description: "למד על פורמט קובץ SSP וממשקי API שיכולים ליצור ולפתוח קובצי SSP."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## מהו קובץ SSP?

קובץ עם סיומת ssp הוא דף אינטרנט שנוצר עם קוד Scala עבור ביטויים במקום HTML רגיל בלבד. הוא פועל כסקריפט בצד השרת תוך שימוש בשילוב של HTML ו-Scala. קבצים אלה נמצאים בשרת ומשמשים ליצירת דפי אינטרנט סטטיים שיוגשו למשתמשים. Scala עצמה היא שפת תכנות למטרות כלליות שהתחביר שלה מוכר למשתמשים שעבדו עם Velocity, JSP או Erb. ניתן לנתח ולהעריך קובצי SSP באמצעות [Scalate](https://scalate.github.io/scalate/) שהוא מנוע תבנית מבוסס Scala להפקת טקסט וסימון.

## פורמט קובץ SSP - מידע נוסף

קובצי SSP נשמרים בקובץ טקסט רגיל וניתן להעריך אותם באמצעות Scalate. תבנית Ssp מורכבת מטקסט רגיל שהוא לעתים קרובות יותר מסמך ה-HTML. יש בו תגי Ssp שגורמים למנועי הרינדור לעבד חלקים שונים של המסמך באופן דינמי. התגים מתחילים ומסתיימים ברצף <% ... %> ו-${ ... } וכל מה שמחוץ להם נחשב כטקסט מילולי.

### דוגמה ל-SSP

הדוגמה הבאה מציגה את קוד SSP והפלט שלו כאשר הוא מעובד על ידי מנוע העיבוד.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
הפלט הוא כדלקמן.
```
<p>
  hi there reader!
  yo 7
</p>
```

## הפניות

- [SSP Reference](https://scalate.github.io/scalate/documentation/ssp-reference.html)

