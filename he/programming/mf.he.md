{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - פורמט קובץ מניפסט של Java",
  "description":"למד על פורמט קובץ MF וממשקי API שיכולים ליצור ולפתוח קבצי MF.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## מהו קובץ MF?

קובץ עם סיומת .mf הוא קובץ Java Manifest המכיל מידע על ערכי הקובץ [JAR](/he/programming/jar/) הבודדים. קובץ ה-MF עצמו כלול בתוך קובץ JAR ומספק את כל ההגדרות הקשורות להרחבות ולחבילה. ניתן לייצר קובצי JAR לשימוש כקובץ הפעלה. במקרה כזה, קובץ mainfest מציין את המחלקה הראשית של האפליקציה המכילה את הצהרת **`public static void main`**. קובצי מניפסט נקראים MANIFEST.MF וניתן לפתוח אותם עם כל עורך טקסט במערכות ההפעלה Windows, MacOS ו-Linux.

## מפרטי פורמט קובץ מניפסט

[מפרט פורמט קובץ Manifest](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) זמינים על ידי Oracle במדריך שלהם לפורמט קובץ JAR. קובץ מניפסט מורכב מקטעים עיקריים שאחריהם מופיעה רשימה של קטעים עבור ערכי קובץ JAR בודדים. כל סעיף עוקב אחר כמה כללים והגבלות.

### חלקים ראשיים

חלק מרכזי:

* מכיל מידע על אבטחה ותצורה על קובץ JAR
* מכיל מידע על האפליקציה או ההרחבה שקובץ JAR הוא חלק ממנה
* מגדיר את התכונות העיקריות עבור כל פריט מניפסט בודד

**הערה**: לא ניתן לקרוא לתכונה בסעיף זה "שם".

### קטעים בודדים

קטע בודד מגדיר תכונות שונות עבור חבילות או קבצים של קובץ JAR. כל קטע חייב להתחיל בתכונה בשם "שם" שהערך שלה חייב להיות נתיב יחסי לקובץ, או כתובת URL מוחלטת שמפנה לנתונים מחוץ לארכיון.

### מפרטי מניפסט

|מאפיינים|תיאור|
---|---|
|manifest-file|main-section newline *מדור-יחיד|
|main-section|גרסה חדשה שורה *main-attribute|
|version-info|Manifest-Version: גרסה-מספר|
|גרסה-מספר|ספרה+{.digit+}*|
|main-attribute|(כל תכונה ראשית לגיטימית) newline|
|individual-section|שם: ערך newline *perentry-attribute|
|perentry-attribute|(כל תכונה perentry לגיטימית) newline|
|newline|CR LF | LF | CR (לא אחריו LF)|
|ספרה|{0-9}|

## הפניות

* [Oracle - פורמט קובץ JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [פורמט קובץ JAR](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20distribution.&text=They%20are%20built%20on%20the,jar%20file%20extension.)

