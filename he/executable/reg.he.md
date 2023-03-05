{
  "date" : "2021-08-02",
  "keywords" :[ "קובץ reg", "פורמט קובץ reg", "מהו קובץ reg", "קובץ", "דוגמה של reg", "סיומת קובץ reg", "סיומת", "פורמט" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ REG וממשקי API שיכולים ליצור ולפתוח קובצי REG.",
  "title" :"REG - קובץ הרישום של Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## מהו קובץ REG?
קובץ REG הוא פשוט קובץ טקסט עם סיומת .reg. קבצים אלה נוצרים בדרך כלל על ידי ייצוא מפתחות טיפוסיים מהרישום. קבצים אלה יכולים לשמש גם כגיבוי של הרישום (במיוחד שלב זה חשוב לפני ביצוע שינויים!). אתה יכול לראות שחלקם הפכו אותם לזמינים כקבצים להורדה באותם אתרים שמראים לך כיצד לבצע פריצת Registry. קובץ REG שימושי בביצוע שינויים ידניים ברישום ולייצא את השינויים הללו. פשוט נקה מעט את הקובץ ולאחר מכן שתף אותו עם אחרים.

## פורמט קובץ REG
פורמט הקובץ REG תוכנן לייצוא ויבוא חלקים של הרישום של Windows באמצעות תחביר מבוסס INI. רישום Windows הוא מסד נתונים יחסי או היררכי ששומר על ההגדרות ברמה נמוכה עבור מערכת ההפעלה Microsoft Windows ויישומים אחרים המשתמשים ברישום Windows. לחלופין, אנו יכולים לומר, הרישום או הרישום של Windows מורכבים ממידע, אפשרויות, הגדרות וערכים אחרים עבור תוכניות וחומרה המותקנות בכל הגירסאות של מערכות ההפעלה Microsoft Windows.
### תחביר של קובץ REG
להלן כמה אלמנטים מרכזיים כחלק של תחביר קובץ REG:
- **RegistryEditorVersion**: למשל "עורך הרישום של Windows גרסה 5.00" עבור Windows 2000, Windows XP ו-Windows Server 2003.
- **שורה ריקה**: מזהה את ההתחלה של נתיב רישום חדש.
- **RegistryPathx**: הנתיב של מפתח המשנה שמכיל את הערך הראשון שאתה מייבא.
- **DataItemNamex**: השם של פריט הנתונים שברצונך לייבא.
- **DataTypex**: סוג הנתונים עבור ערך הרישום.

המפתחות מאוחסנים בקבצי reg באמצעות התחביר הבא:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
אתה יכול לערוך את ערך ברירת המחדל של מפתח באמצעות "@" במקום "שם ערך":
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### דוגמא
הנה דוגמה לקובץ REG
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## הפניות

* [רישום Windows- מאת ויקיפדיה](https://en.wikipedia.org/wiki/Windows_Registry)
* [כיצד להוסיף, לשנות או למחוק מפתחות משנה וערכי רישום באמצעות קובץ ‎.reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)
