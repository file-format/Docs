{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "הרחבה", "קובץ", "פורמט קובץ", "סוג קובץ מסד נתונים", "פורמט קובץ מסד נתונים", "קבצי מסד נתונים" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ SQLITE וממשקי API שיכולים ליצור ולפתוח קבצי SQLITE.",
  "title" :"פורמט קובץ SQLite",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## מהו קובץ SQLite?

קובץ עם סיומת .sqlite הוא קובץ מסד נתונים SQL קל משקל שנוצר באמצעות תוכנת [SQLite](https://www.sqlite.org/index.html). זהו מסד נתונים בקובץ עצמו ומיישם מנוע מסד נתונים [SQL](/he/database/sql/) עצמאי, בעל תכונות מלאות, אמין ביותר. ניתן להשתמש בקבצי מסד נתונים של SQLite כדי לשתף תוכן עשיר בין מערכות על ידי החלפה פשוטה של קבצים אלה ברשת. כמעט כל הניידים והמחשבים משתמשים ב-SQLite לאחסון ושיתוף נתונים, והוא הבחירה בפורמט הקובץ עבור יישומים חוצי פלטפורמה. בשל השימוש הקומפקטי והשימושיות הקלה שלו, הוא מגיע עם יישומים אחרים. קיימות כריכות SQLite לשפות תכנות כגון C, [C#](/he/programming/cs), [C++](/he/programming/cpp), [Java](/he/programming/java/), [PHP](/he/programming/php/ ), ורבים אחרים.

## פורמט קובץ SQLite

SQLite במציאות היא ספריית C-Language המיישמת את SQLite RDBMS באמצעות פורמט הקובץ SQLite. עם ההתפתחות של מכשירים חדשים מדי יום, פורמט הקובץ שלו נשמר תואם לאחור כדי להתאים למכשירים ישנים יותר. פורמט קובץ SQLite נתפס כפורמט ארכיון ארוך טווח עבור הנתונים.

### קובץ מסד הנתונים

מסד נתונים של SQLite מתוחזק במלואו באמצעות שני קבצים.
* קובץ מסד נתונים ראשי - מכיל מצב מלא של מסד הנתונים של SQLite
* יומן החזרה - מאחסן מידע נוסף בקובץ שני ומשמש במהלך ביצוע עסקאות. במקרה של SQLite במצב WAL, קובץ יומן ראשי כתיבה נשמר.

#### קובץ יומן

קובץ זה נועד לשמור את כל המידע שמור למקרה שלא ניתן היה להשלים את העסקה האחרונה במקרים כגון קריסת מחשב. קובץ זה משמש לשחזור קובץ מסד הנתונים למצב עקבי.

#### דפים

קובץ מסד הנתונים הראשי של SQLite מורכב מעמוד אחד או יותר. בכל נקודת זמן, לכל עמוד במסד הנתונים הראשי יש שימוש יחיד שהוא אחד מהבאים:

* דף הנעילה-בייט
* דף רשימות חופשיות
* דף תא מטען חופשי
* דף דף דף חופשי
* דף עץ b
* דף פנים b-tree שולחן
* דף עלה עץ b שולחן
* דף פנים B-tree אינדקס
* דף עלה עץ אינדקס
* דף הצפת מטען
* דף מפת מצביע

הגודל של קבצי מסד נתונים של SQLite יכול לנוע בין קילובייט בודדים לכמה גיגה-בייט.

### כותרת SQLite

כותרת מסד הנתונים של SQLite ממוקמת ב-100 הבתים הראשונים של קובץ מסד הנתונים. כל קובץ מסד נתונים חוקי של SQLite מתחיל ב-16 בתים (ב-hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. הפרטים של שדות הכותרת הם כמו בטבלה הבאה.

|היסט|גודל|תיאור|
---|---|---|
|0|16|מחרוזת הכותרת: "SQLite format 3\000"|
|16|2|גודל עמוד מסד הנתונים בבתים. חייב להיות חזקה של שתיים בין 512 ל-32768 כולל, או שהערך 1 מייצג גודל עמוד של 65536.|
|18|1|גרסת כתיבת פורמט קובץ. 1 עבור מורשת; 2 עבור WAL.|
|19|1|גרסת קריאה של פורמט קובץ. 1 עבור מורשת; 2 עבור WAL.|
|20|1|בייטים של שטח "שמור" לא בשימוש בסוף כל עמוד. בדרך כלל 0.|
|21|1|שבר מטען משובץ מקסימלי. חייב להיות 64.|
|22|1|חלק מינימלי של מטען משובץ. חייב להיות 32.|
|23|1|שבר מטען עלה. חייב להיות 32.|
|24|4|מונה שינוי קבצים.|
|28|4|גודל קובץ מסד הנתונים בדפים. "גודל מסד הנתונים ב-header".|
|32|4|מספר עמוד של עמוד המטען הראשון של הרשימה החופשית.|
|36|4|מספר כולל של דפי רשימות חופשיות.|
|40|4|עוגיית הסכימה.|
|44|4|מספר פורמט הסכימה. פורמטים של סכימה נתמכים הם 1, 2, 3 ו-4.|
|48|4|גודל מטמון דף ברירת מחדל.|
|52|4|מספר העמוד של עמוד השורש הגדול ביותר של עץ b כאשר הוא נמצא במצב ואקום אוטומטי או אינקרמנטלי-וואקום, או אפס אחרת.|
|56|4|קידוד טקסט מסד הנתונים. ערך 1 פירושו UTF-8. ערך של 2 פירושו UTF-16le. ערך של 3 פירושו UTF-16be.|
|60|4|"גרסת המשתמש" כפי שנקראה ונקבעה על ידי הפרגמה של user_version.|
|64|4|True (לא אפס) עבור מצב ואקום אינקרמנטלי. שקר (אפס) אחרת.|
|68|4|"מזהה האפליקציה" שהוגדר על ידי PRAGMA application_id.|
|72|20|שמור להרחבה. חייב להיות אפס.|
|92|4|מספר הגרסה-תקף-עבור.|
|96|4|SQLITE_VERSION_NUMBER|

## הפניות ##

* [פורמט קובץ SQLite - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - ויקיפדיה](https://en.wikipedia.org/wiki/SQLite)
* [SQLite - מפרט שפת C](https://www.sqlite.org/c3ref/intro.html)
