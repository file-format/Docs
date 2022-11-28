{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Unix Manual",
  "description":"למד על פורמט קובץ FODT וממשקי API שיכולים ליצור ולפתוח קבצי MAN.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## מהו קובץ MAN?

קובץ עם סיומת .man מייצג man page שהוא מדריך למשתמש לתכנות יוניקס בצורת תיעוד תוכנה. הוא משמש את כלי השירות `Man`, הכלול ב-Unix, המשמש לצפייה בתיעוד. תיעוד התוכנה מכיל מידע במקטעים ובעמודים שניתן לאחזר באמצעות כלי השירות Man ממסוף הפקודות על ידי הוצאת פקודות. בהיותו זמין במחשב כעותק רך של התיעוד, אין צורך בשום עותק מודפס או חיבור לאינטרנט כדי לגשת אליו.

## Unix Manual Man Format File - מידע נוסף

דפי אדם מאוחסנים בפורמט טקסט רגיל וניתן ליצור אותם ולפתוח אותם בכל עורך טקסט לצפייה או עריכה. ב-UNIX, מידע מדפי האיש מאוחזר על ידי הוצאת פקודות מהמסוף הכוללות הפניה למספרי סעיפים ועמודים מהמדריך.

### מדורים ודפים

Unix man הוא המדריך של המערכת שבו כל ארגומנט עמוד לפקודה מתייחס לשם של תוכנית, שירות או פונקציה. הפקודה, אם היא מסופקת עם מידע על המדור, תחפש את הדף במקטע הספציפי הזה. עם זאת, התנהגות ברירת המחדל היא לחפש את הדף בכל המקטעים ולהציג את העמוד הראשון ללא קשר אם הוא קיים במספר חלקים.

### מספרי סעיפים

להלן המידע על מספרי הסעיפים של המדריך ואחריו סוגי הדפים שהם מכילים.

|מספר מדור|סוג הדפים|
---|---|
|1|תוכניות ניתנות להפעלה או פקודות מעטפת|
|2|קריאות מערכת (פונקציות שמסופקות על ידי הליבה)|
|3|שיחות ספרייה (פונקציות בתוך ספריות תוכניות)|
|4|קבצים מיוחדים (נמצאים בדרך כלל ב-/dev)|
|5|פורמטים ומוסכמות של קבצים, למשל /etc/passwd|
|6|משחקים|
|7|שונות (כולל חבילות מאקרו ומוסכמות), למשל man(7), groff(7)|
|8|פקודות ניהול מערכת (בדרך כלל רק עבור root)|
|9|שגרות ליבה [לא סטנדרטיות]|

## דוגמה - כיצד לקרוא דפי MAN?

הנה דוגמה כיצד לאחזר מידע על פקודת MkDir באמצעות הפקודה Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## הפניות

* [מפרט טכני של OpenDocument - מאת ויקיפדיה](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) - דף מדריך לינוקס](https://man7.org/linux/man-pages/man1/man.1.html)

