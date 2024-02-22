{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "למד על פורמט קובץ ABCDDB וממשקי API שיכולים ליצור ולפתוח קבצי ABCDDB.",
  "title" : "פורמט קובץ ABCDDB - קובץ מסד הנתונים של רשימת אנשי הקשר של פנקס הכתובות של Apple",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-he",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## מהו קובץ ABCDDB?

הקובץ עם הסיומת **.ABCDDB** מייצג Apple Address Book Contact List Database. זה שייך ליישום **פנקס כתובות** הידוע גם בשם **אנשי קשר**. זהו יישום מובנה וכלול במערכות ההפעלה iOS ו-macOS. אפליקציית אנשי הקשר מאפשרת למשתמשים לשמור ולארגן מידע הקשור לאנשי הקשר שלהם, כולל אנשים, עסקים וארגונים. אפליקציה זו מאפשרת למשתמשים לעקוב אחר פרטים כגון שמות, כתובות, מספרי טלפון וכתובות דואר אלקטרוני, כמו גם לסווג את אנשי הקשר שלהם לקבוצות.

## קשר עם SQLite ו-Typical Path

פנקס הכתובות של אפל (הידוע גם בשם אנשי קשר) מאחסן את פרטי הקשר ככרטיסי vCard בתיקיית המטא נתונים. **הקובץ _ABCDDB_ הוא למעשה _SQLite 3 datafile_**.

SQLite היא מערכת פופולרית לניהול מסדי נתונים שנועדה להיות קלת משקל ועצמאית. הוא משמש בהרבה סוגים שונים של תוכנות והתקנים. SQLite הוא סוג של RDBMS, כלומר הוא מאחסן נתונים בטבלאות הקשורות זו לזו באמצעות מפתחות. הוא יכול להתמודד עם מגוון סוגי נתונים, כולל מספרים שלמים, מספרי נקודה צפה, מחרוזות ונתונים בינאריים. בנוסף, SQLite תומך בטרנזקציות, המאפשרות למשתמשים לבצע מספר פעולות מסד נתונים יחד כיחידת עבודה אחת.

הקובץ עם סיומת ABCDDB מאוחסן כאן בדרך כלל

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## תיקון מסד נתונים פגום של אנשי קשר

אנא קח תחילה את הגיבוי לפני שתנסה לעשות זאת. אז נא לנווט אל

`~/Library/Application Support/AddressBook`

בספרייה זו, תמצא שלושה קבצים כולל זה עם סיומת .abcddb

- `פנקס כתובות-v22.abcddb`
- `פנקס כתובות-v22.abcddb-wal`
- `פנקס כתובות-v22.abcddb-shm`

מחק את כל הקבצים האלה ופתח מחדש את אנשי הקשר זה יתחיל לעבוד שוב.

## שחזר את מסד הנתונים של ספר הכתובות מגיבוי

נניח שאנשי הקשר שלך במסד הנתונים של פנקס הכתובות מאוחסנים ב-'כתובות-v22.abcddb

- תחילה גבה את נתוני ספר הכתובות שלך וצא מכל היישומים.
- העבר את קובץ מסד הנתונים שלך לתיקיית המשנה `~/Library/Application Support/AddressBook`
- הפעל את **Book.app**.

## ייצוא נתוני קובץ ABCDDB ל- Microsoft Access

מכיוון שהקובץ הוא SQLite 3 datafile, אתה יכול לייצא את הנתונים בתוך קובץ abcddb לתוך Microsoft Access באמצעות מחבר ODBC.

מחבר SQLite ODBC הוא ספריית תוכנה ומנהל התקן המאפשרים ליישומים התומכים בממשק ODBC להתחבר למסד נתונים של SQLite. הוא כולל ספרייה המגדירה את ממשק ODBC, ומנהל התקן שמתרגם את הממשק הזה לקריאות ל-SQLite API. כדי להשתמש במחבר SQLite ODBC, תחילה עליך להתקין אותו ולאחר מכן להגדיר מקור נתונים ODBC במחשב שלך. לאחר השלמת השלבים הללו, כל אפליקציה המצוידת בתמיכה ב-ODBC תוכל להתחבר למקור הנתונים ולאחזר נתונים ממסד הנתונים של SQLite.

## הפניות
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [מסד נתונים של אנשי קשר עבור Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [כיצד אוכל לפתוח או לייצא קובץ abcddb ב-Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

