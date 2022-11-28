{
  "date" : "2021-06-09",
  "keywords" :[ "רמז", "קובץ", "הרחבה", "פורמט", "מהו קובץ רמז", "מוזיקה", "פורמט קובץ רמז", "מפרט פורמט קובץ רמז", "גיליון רמז", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ CUE וממשקי API שיכולים ליצור, להמיר ולפתוח קובצי CUE.",
  "title" :"CUE - קובץ גיליון רמז",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## מהו קובץ CUE?

קובץ עם סיומת .cue, הידוע גם כקובץ cue sheet, הוא קובץ מטא נתונים המכיל מידע על פריסת הרצועות בתקליטור או DVD. אלה נתמכים על ידי נגני מדיה ויישומים ליצירת דיסקים אופטיים. נתוני האודיו העיקריים המאוחסנים בתקליטור מופנים על ידי קובץ ה-cue, יחד עם מפרטי אורכי הרצועה, כותרות הדיסקים והמבצעים. לפיכך, אם קובץ שמע בודד מכיל מספר רצועות, ניתן להשתמש בקובץ ה-cue כדי לחלק את השמע למספר קבצים או להפנות לרצועות שונות.

## פורמט קובץ CUE

קבצי CUE או קובצי גיליון רמז מאוחסנים בפורמט טקסט רגיל הניתן לקריאה אנושית. מידע בקובץ cue הם פקודות עם פרמטר אחד או יותר. פקודות אלו חלות על הקובץ כולו או על רצועה בודדת, בהתאם לפקודה הספציפית ולהקשר. המדריך למשתמש של CDRWIN מתאר את המפרטים של תחביר גיליון ה-cue והסמנטיקה.

## פקודות חיוניות של גיליון CUE

|פקודה|תיאור|
---|---|
|קובץ| הכוונה לקובץ המכיל את הנתונים והפורמט שלו כגון [MP3](/he/audio/mp3/), [WAV](/he/audio/wav/), או תמונת דיסק בינארי רגיל)|
|TRACK| מגדיר את מידע הקשר הרצועה כגון מספרו וסוגו או מצבו.|
|אינדקס| מייצג את המיקום כאינדקס בתוך ה-FILE. הפורמט הוא mm:ss:ff (דקה-שנייה-פריים).|
|PREGAP ו-POSTGAP|זה מציין את הפער המקדים או ה-post-gap של רצועה, שאינה מאוחסנת בשום קובץ נתונים. האורך מצוין באותו פורמט דקה-שנייה-פריים כמו עבור INDEX.|

### דוגמה לגיליון CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## הפניות

* [קובץ cda - מאת ויקיפדיה](https://en.wikipedia.org/wiki/.cda_file)

