{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "הרחבה", "קובץ", "פורמט קובץ", "סוג קובץ מסד נתונים", "פורמט קובץ מסד נתונים", "קבצי מסד נתונים" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ MDB וממשקי API שיכולים ליצור ולפתוח קובצי MDB.",
  "title" :"פורמט קובץ MDB - קובץ מסד נתונים של Microsoft Access",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## מהו קובץ MDB?

קובץ עם סיומת .mdb הוא קובץ מסד נתונים של Microsoft Access שהוא מערכת ניהול מסד נתונים יחסי (RDBMS). הוא מאחסן נתונים בטבלאות מסד נתונים המקושרות זו לזו באמצעות מפתחות ראשיים וזרים. קובץ ה-MDB מכיל את המבנה המלא של טבלאות מסד הנתונים, שאילתות, נהלים מאוחסנים. MDB הוא פורמט הקובץ המוגדר כברירת מחדל עבור Microsoft Access 2003. הגירסאות הרוחביות של Microsoft Access משתמשות בתבניות הקובץ [ACCDB](/he/database/accdb/) שהיא פורמט הקובץ העדכני ביותר עד כה. ניתן לפתוח קבצי MDB עם יישומים כמו Microsoft Access, MDB Viewer, MDBOpener, וניתן להמיר אותם ל-ACCDB, [CSV](/he/spreadsheet/csv/), פורמטים של Excel וכו'.

## פורמט קובץ MDB

ישנם מפרטים ציבוריים זמינים עבור פורמט MDB והוא נשאר פורמט הקובץ הקנייני של מיקרוסופט. מיקרוסופט, לעומת זאת, מספקת גישת קישוריות לקובץ ה-MDB באמצעות תקן Open Database Connectivity (ODBC) ו-Visual Basic for Applications (VBA). מדריך ה-MDB הלא רשמי מספק תיאור קצר ובלתי פורמלי של פורמט ה-MDB המבוסס על הנדסה לאחור וניתן להתייעץ איתו כדי לדעת על המפרט.

### דפים

לפי מדריך ה-MDB הלא רשמי, קובץ MDB מורכב מדפים בגודל קבוע (2048 בתים עבור Jeb DB3 ו-4096 בייטים עבור Jet DB 4). הבית הראשון מציין את סוג העמוד. להלן סוגי הדפים העיקריים:

`עמוד ראשון:` הוא מכיל מידע על כותרות של מסד נתונים הכולל גם את הזיהוי של גרסת Jet DB שאליה הקובץ תואם. בנוסף, הוא כולל גם מידע אבטחת קבצים ומפה של שימוש בדף.

`דף הגדרות טבלה:` דף הגדרת טבלה מציין עמודות, סוגי נתונים, אינדקס ומידע אחר. הוא משתמש בדפים נוספים במידת הצורך וכולל מפה של דפים המכילה את נתוני השורות של טבלה זו.

`דפי נתונים:` דפי הנתונים הם מיכלי הנתונים בפועל שבהם הנתונים מאוחסנים לפי שורות. הוא משתמש בדפי בת כדי לאחסן ערכי נתונים ארוכים.

מסד נתונים יחיד של Microsoft Access עשוי להכיל מספר קבצים המאפשרים לחרוג ממגבלות גודל הקבצים והטבלה. זה מאפשר לשים טפסים וקוד בקובץ MDB חזיתי על שולחן העבודה של המשתמש ונתונים בקבצי MDB אחורי אחר בשרתים המחוברים לרשת.

## הפניות ##

* [מפרטי גישה](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [מדריך ה-MDB הלא רשמי](http://jabakobob.net/mdb/)
