{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ NMONEY וממשקי API שיכולים ליצור ולפתוח קבצי NMONEY.",
  "title" :"קובץ NMONEY - פורמט קובץ חשבון Denaro",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## מהו קובץ NMONEY?

קובץ NMONEY הוא קובץ מסד נתונים לאחסון נתונים פיננסיים המכיל רקורד של עסקאות פיננסיות. זה פותח על ידי Nickvision והיה בשימוש בתוכנת Nickvision Denaro שהיא יישום תוכנה פיננסית אישית. נתונים המאוחסנים בתוך קובץ NOMONEY כוללים פרטי עסקאות אשראי וחיוב לחשבון.

ניתן לפתוח קבצי NOMONEY באמצעות יישום [Github](https://github.com/NickvisionApps/Denaro).

## על תוכנת Denaro

Denaro פותחה בתחילה על ידי [Nickvision](https://nickvision.org/) כמוצר שהומר מאוחר יותר לאפליקציית תוכנה בקוד פתוח המתארחת ב-[Github](https://github.com/NickvisionApps/Denaro) . מאז האפליקציה שונתה ועודכנה ב-Github בלבד. האפליקציה מפותחת ב-C# בממשק המשתמש של Windows עם Windows App SDK (WinUI 3 כמו בשלב זה).

### תכונות המוצעות על ידי Denaro

* נהל מספר חשבונות בו זמנית עם ממשק הכרטיסיות הפופולרי והמוכר ביותר שלו
* סנן עסקאות לפי סוג, קבוצה או תאריך
* פעולות חוזרות כמו חשבונות המתרחשים מדי חודש
* העברת כסף מחשבון אחד למשנהו
* ייצא את הנתונים מחשבון כקובץ CSV וייבא קובץ CSV, OFX או QIF כדי להוסיף עסקאות לחשבון

## פורמט קובץ Denaro - מידע נוסף

קבצי Denaro נשמרים על דיסק בפורמט קובץ בינארי. נתונים פיננסיים מאוחסנים כקובץ מסד נתונים בפורמט קובץ **.SQLITE3**. SQLITE הוא קובץ מסד נתונים SQL קל משקל שנוצר עם תוכנת SQLite. הוא מספק מנוע מסד נתונים עצמאי המסוגל לספק מסד נתונים מלא ואמין ביותר. ניתן להשתמש בקבצי מסד נתונים של SQLite כדי לשתף תוכן עשיר בין מערכות פשוט על ידי החלפת קבצים אלה דרך הרשת. קיימות כריכות SQLite לשפות תכנות כגון C, [C#](/he/programming/cs/), [C++](/he/programming/cpp/), [Java](/he/programming/java/), [PHP](/he/programming/ php/), ועוד רבים אחרים.

## הפניות

* [Nickvision](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

