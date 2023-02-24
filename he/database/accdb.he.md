{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "הרחבה", "קובץ", "פורמט קובץ", "סוג קובץ מסד נתונים", "פורמט קובץ מסד נתונים", "קבצי מסד נתונים" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ ACCDB וממשקי API שיכולים ליצור ולפתוח קבצי ACCDB.",
  "title" :"פורמט קובץ ACCDB - קובץ מסד הנתונים של Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## מהו קובץ ACCDB?

קובץ עם סיומת .accdb הוא קובץ מסד נתונים של Microsoft Access 2007 המאחסן את נתוני המשתמשים בטבלאות. זה תומך באחסון
טפסים מותאמים אישית, שאילתות SQL ונתונים אחרים. קבצי ACCDB החליפו קבצי [MDB](/he/database/mdb/) לאחר ש-Microsoft עברה למבנה קבצים מבוסס XML. עדיין ניתן להמיר קבצי ACCDB ל-MDB עם תאימות ישנה. עם זאת, ה-ACCDB הם פורמט קובץ מסד הנתונים של Access בשימוש נרחב כעת. מיקרוסופט תמכה גם בתכונות נוספות בפורמט ACCDB כגון אפשרות לאחסן קבצים מצורפים, נתונים בינאריים ותמיכה בשדה רב-ערכים.

## פורמט קובץ ACCDB

כמו MDB, אין מפרטים ציבוריים זמינים עבור פורמט קובץ ACCDB. מיקרוסופט תומכת בגישה לקבצים אלה באופן פרוגרמטי באמצעות תקן Open Database Connectivity (ODBC) ו-Visual Basic for Applications (VBA).

### תובנה

dump hex של קובץ ACCDB פשוט מצביע על דמיון כללי במבנה לגרסאות האחרונות של משפחת ה-MDB Format Family הקודמת. שני פורמטי הקבצים משתמשים בגדלים קבועים של עמודים של 4096 בתים. דמיון נוסף בין ACCDB ל-MDB הוא צורת המספר הקסום, הכולל את המחרוזת "Standard ACE DB" עבור ACCDB. גרסה או קוד תאימות נמצאים באותו מיקום בשני הפורמטים. ה-mdbtools | קובץ ה-HACKING אומר "Offset 0x14 מכיל את גרסת Jet של מסד נתונים זה" ו-MDB המדריך הלא רשמי מסכים. המידע במקורות אלה, בשילוב עם ערך ויקיפדיה עבור [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), מצביע על כך שערך של 0x02 מציין ACE 12 (Access 2007) ו-0x03 מציין ACE 14 (Access 2010). עם זאת, מסד נתונים מינימלי שנוצר ב-Access 2010 ואחד דומה שנוצר ב-Access 2016, לשניהם יש 0x02 במיקום זה. מסד נתונים מינימלי שנוצר ב-Access 2016, אך הגדרת עמודה עם סוג הנתונים החדש "מספר שלם גדול", היה בעל ערך של 0x05. בקבצי ACCDB, נראה שמדד זה משקף את התאימות של הקובץ ולא את הגרסה של מנוע ה-ACE המשמש ליצירתו.

## הפניות

* [פורמט קובץ גישה](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?redirectSourcePath=% 252fen-us%252farticle%252fIntroduction-to-the-Access-2007-file-format-8cf93630-0b68-4a40-a13c-7528b9f074b6&ui=en-US&rs=en-US&ad=US)
* [Access 2016 Specifications](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [מנוע מסד הנתונים של Microsoft Jet](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [באיזה פורמט קובץ Access עלי להשתמש?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)
