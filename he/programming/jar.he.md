{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar","מהו קובץ jar","כיצד לפתוח קובץ jar", "סיומת", "קובץ", "קובץ jar","פורמט קובץ jar", "סיומת jar" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - פורמט קובץ ארכיון Java",
  "description":"למד על פורמט קובץ JAR וממשקי API שיכולים ליצור ולפתוח קובץ JAR.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## מהו קובץ JAR?

קובץ עם סיומת jar הוא קובץ Java Archive המכיל קבצים רבים ושונים הקשורים לאפליקציות כקובץ בודד. פורמט קובץ זה נוצר כדי להפחית את מהירות הטעינה של יישומון Java שהורד בדפדפן באמצעות עסקת HTTP, על ידי הימנעות מיצירת חיבורי HTTP מרובים. קובץ JAR בודד יכול להכיל קבצי Java Class ([.class](/he/programming/class/)), [images](/he/image/) ו-[sounds](/he/audio/). פריטים בודדים בתוך קובץ JAR יכולים להיות חתומים דיגיטלית על ידי מפתח האפליקציה כדי לאמת את מקורם. קבצי JAR משמשים באופן קבוע ליצירת ממשקי API פונקציונליים המכילים פונקציונליות ספציפית הקשורה לאותו API.

## פורמט קובץ JAR

קובצי JAR מבוססים על [פורמט קובץ ה-ZIP] הפופולרי (/he/compression/zip/) המאחסן את קובצי התוכן הבודדים שלו בקובץ בודד. פורמט קובץ JAR תומך בדחיסות, וכתוצאה מכך גודל קובץ קטן יותר להורדה, ולכן משפר עוד יותר את זמן ההורדה. [מפרטי קובץ JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) מאת Oracle מספק פרטים מלאים על המפרט הפנימי של קובצי JAR.

### קובץ המניפסט

כאשר נוצר קובץ JAR, נוצר בתוכו אוטומטית קובץ מניפסט המכיל את מידע המטא נתונים על התוכן של קובץ JAR. קובץ זה מציג את התוכן שנארז בתוך קובץ JAR. קובץ Manifest טיפוסי נראה כדלקמן המציג את התיקיות והמחלקות הכלולים בקובץ JAR.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### מפרטי מניפסט

מפרטי מניפסט מוגדרים על ידי Oracle כדלקמן.

`manifest-file`: קטע ראשי בשורה חדשה \*מקטע יחיד

`main-section`: info version newline \*main-attribute

`version-info`: Manifest-Version: גרסה-מספר

`version-number` : ספרה+{.digit+}*

`main-attribute`: (כל תכונה ראשית לגיטימית) שורה חדשה

`individual-section`: שם: ערך newline \*perentry-attribute

`perentry-attribute`: (כל תכונת perentry לגיטימית) שורה חדשה

`קו חדש` : CR LF | LF | CR (לא אחריו LF)

`digit`: {0-9}

### JAR בר הפעלה

קובצי JAR יכולים להכיל גם יישום שניתן להפעיל על ידי Java Virtual Machine (JVM) בדומה לכל יישום אחר במערכת ההפעלה Microsoft Windows. במקרה זה, ה-JVM צריך לדעת על נקודת הכניסה של האפליקציה שהיא כל מחלקה עם שיטה ראשית של ריקון סטטי ציבורי. קובץ המניפסט מזהה מחלקה כזו עם הכותרת 'Main-Class' בפורמט הבא:

```
Main-Class: com.example.MyClassName
```



## הפניות

* [סקירת קובץ JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [פורמט קובץ JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

