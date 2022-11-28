{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ AGI - פורמט קובץ ממשק שער כוכבית",
  "description":"למד על פורמט קובץ AGI עם דוגמה וממשקי API שיכולים ליצור ולפתוח קובצי AGI.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## מהו קובץ AGI?

קובץ AGI הוא קובץ סקריפט המשמש את מערכת הטלפוניה בקוד פתוח, Asterisk. הוא מכיל מידע שניתן להשתמש בו כדי להפוך תהליכים לאוטומטיים ולתוכנית חיוג של Asterisk. באמצעות קובצי סקריפט של AGI, ניתן ליצור חיבורים עם מסדי נתונים יחסיים כגון PostgreSQL או MySQL. בנוסף, ניתן להשתמש בסקריפטים של AGI כדי לגשת גם למשאבים חיצוניים אחרים. סקריפטים של AGI יכולים להעביר את השליטה בתוכנית החיוג לסקריפט חיצוני של AGI, מה שמאפשר לכוכבית לבצע משימות מורכבות.

## פורמט קובץ AGI - מידע נוסף

קובצי סקריפט של AGI נשמרים כקובצי טקסט וניתנים לפתיחה בכל עורך טקסט לביצוע שינויים.

### דפוס סטנדרטי של תקשורת AGI

סקריפט AGI טוען את המשתנים והערכים שלהם שנשלחים אליו על ידי כוכבית. מראה נפוץ של משתנים אלה הוא כדלקמן.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

משתנים אלה מלווה בשורה ריקה שנשלחה על ידי כוכבית, המראה שסקריפט AGI יכול להשתלט על תוכנית החיוג כעת.

### שפת תכנות עבור קבצי סקריפט של AGI

ניתן לכתוב סקריפטים של AGI בדרך כלל ב-Perl, [PHP](/he/programming/php/), [C](/he/programming/c/), Pascal או Bourne Shell.

## הפניות

* [Asterisk AGI Script](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

