---
date: 2022-07-30
מְחַבֵּר:
  display_name: Kashif Iqbal
draft: false
toc: true
title: פורמט קובץ JNLP - מהו קובץ JNP?
linktitle: JNLP
description: "למד על פורמט קובץ JNLP וממשקי API שיכולים ליצור ולפתוח קובצי JNLP."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## מהו קובץ JNLP?

קובץ JNLP הוא קובץ Java Web Start (JWS) המכיל מידע XML להפעלת תוכנית Java דרך הרשת. זה נשמר בפורמט Java Network Launching Protocol (JNLP). הוא משמש את טכנולוגיית Java Web Start (JWS) שהיא טכנולוגיית פריסת יישומים להורדה והרצה של יישום. קובץ JNLP מכיל את הכתובת המרוחקת של השרת שממנו מורידים את התוכנית ומופעלים במחשב המקומי.

## פורמט קובץ JNLP - מידע נוסף

קובצי JNLP נשמרים כקבצי **[XML](/he/web/xml/)** המאוחסנים בפורמט טקסט הניתן לקריאה אנושית. קובץ ה-XML מכיל את המידע המשמש להפעלה והפעלה של יישום Java דרך הרשת. ה-JWS מאפשר לך להפעיל יישומים על ידי לחיצה על הקישור לדף האינטרנט. האפליקציה יורדת למקרה שהיא עדיין לא הורדה במחשב המשתמש.

אורקל הוציאה משימוש את JWS עם שחרורו של Java Platform Standard Edition (JSE) 9. עם זה, קבצי JNLP אינם נתמכים יותר.

### כיצד לפתוח קבצי JNLP?

יישומים שיכולים **לפתוח קובצי JNLP** כוללים את **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** ו-* *GitHub Atom**.

### דוגמה לקובץ JNLP

```
<jnlp spec="1.0" codebase="http://localhost/jws" href="Notepad.jnlp">
   <information>
      <title>Notepad Demo</title>
      <vendor>Sun Microsystems, Inc.</vendor>
   </information>
   <resources>
      <property name="jnlp.publish-url" value="$$context/publish"/>
      <j2se version="1.3+" href="http://java.sun.com/products/autodl/j2se"/>
      <jar href="Notepad.jar"/>
   </resources>
   <application-desc main-class="Notepad"/>
</jnlp>
```
**נוֹהָג**

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<HTML>
<HEAD>
   <TITLE>Java Web Start Demo</TTLE>    
</HEAD>
<BODY>

<H1>Java Web Start Demo</H1>
<a href="Notepad.jnlp">Lanuch Notepad Application</a>
This link is to the Notepad.jnlp file.
</BODY>
</HTML>
```
## כיצד להפעיל קבצי JNLP?

עם הוצאה משימוש של JWS, לא ניתן להפעיל יישומים שפותחו על בסיס טכנולוגיית JWS עם הגרסה העדכנית ביותר של Java. עם זאת, ניתן להפעיל תוכניות מבוססות JNLP אלו באמצעות OpenWebStart שהוא יישום מחדש של קוד פתוח של טכנולוגיית Java Web Start. הוא מותקן במקביל לגרסה העדכנית ביותר של Java ומספק את התכונות הנפוצות ביותר של Java Web Start ותקן JNLP.

## הפניות ##

* [מהו Java Web Start וכיצד הוא מושק?](https://www.java.com/en/download/help/java_webstart.html)
* [הפעל JNLP עם הגרסה האחרונה של Java](https://openwebstart.com/)
* [Java Web Start - ויקיפדיה](https://en.wikipedia.org/wiki/Java_Web_Start)

