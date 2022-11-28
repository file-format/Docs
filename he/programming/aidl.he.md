{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ AIDL - קובץ שפה של ממשק אנדרואיד",
  "description":"למד על פורמט קובץ AIDL עם דוגמה וממשקי API שיכולים ליצור ולפתוח קובצי AIDL.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## מהו קובץ AIDL?

קובץ AIDL (Android Interface Definition Language) מאפשר למפתחי אנדרואיד ליצור תקשורת בין אפליקציות שונות. בהתבסס על ממשק התכנות, גם הלקוח וגם השירות מסכימים לתקשר באמצעות תקשורת בין-תהליכית (IPC). קובץ AIDL מכיל קוד מקור [Java](/he/programming/java/) להגדרת ממשקים אלה וחוזים לתקשורת בין אפליקציות.

אתה יכול לפתוח קבצי AIDL עם Google Android Studio או כל עורך טקסט כגון Microsoft Notepad ו-Notepad++.

## פורמט קובץ AIDL - מידע נוסף

AIDL הם קבצי טקסט המכילים את הממשקים לתקשורת בין אפליקציות. מערכת ההפעלה אנדרואיד אינה מאפשרת לתהליך אחד לגשת לזיכרון של תהליך אחר. זה מוביל את התהליכים לפצל את האובייקטים שלהם לפרימיטיבים להבנת מערכת ההפעלה הבסיסית ולבסס תהליך של מבני תקשורת למפתחים.

### אילו סוגי נתונים נתמכים על ידי AIDL?

AIDL תומך בסוגי הנתונים הבאים כברירת מחדל.

* כל הסוגים הפרימיטיביים בשפת התכנות Java (כגון int, long, char, boolean וכן הלאה)
* מחרוזת
* CharSequence
* רשימה
* מפה

## דוגמה לקובץ AIDL

להלן דוגמה לקובץ AIDL.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## הפניות

* [שפת הגדרת ממשק אנדרואיד (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

