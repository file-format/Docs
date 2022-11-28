{
  "date" : "2021-07-12",
  "keywords" :[ "קובץ cmd", "מהו קובץ cmd", "קובץ", "דוגמה cmd", "סיומת קובץ cmd","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ CMD וממשקי API שיכולים ליצור ולפתוח קובצי CMD.",
  "title" :"CMD - פורמט קובץ הפקודה של Windows",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## מהו קובץ CMD?
קובץ CMD מורכב מסקריפט המכיל פקודה אחת או מרובות בצורת טקסט רגיל המופעלות על מנת לבצע משימות שונות. זה דומה לקובץ [BAT](/he/executable/bat/), המשמש גם בדרך כלל לאחסון אצווה של פקודות ניתנות להפעלה. קבצי CMD נמצאים בשימוש נרחב במערכת ההפעלה Microsoft Windows. קבצים אלה הוצגו כמעט בשנות ה-90 אך עדיין בשימוש במערכת ההפעלה העדכנית ביותר של Windows. קבצים אלה נכתבים בדרך כלל כדי לבצע יותר מפקודה אחת ברצף.

## פורמט קובץ CMD
CMD הוא פורמט קובץ המשמש תוכניות הפעלה בסגנון CP/M. זה בדרך כלל בר השוואה ל-[COM](/he/executable/com/) ב-CP/M-80 ו-[EXE](/he/executable/exe/) ב-DOS. קובץ CMD מכיל 1 עד 8 קבוצות של קוד או נתונים וכותרת של 128 בתים. כל קבוצה יכולה להיות בגודל של עד 1 mb. קבצי CMD יכולים להכיל גם מידע על רילוקיישן ותוספות מערכת תושב (RSX) בגרסאות מאוחרות יותר. ה-CMD הוא עולה חדש בהשוואה לקובץ [BAT](/he/executable/bat/); משמש עבור MS-DOS לפני שחרורו של Windows ב-MS-DOS. למרות שאתה עדיין יכול לשמור קבצים עם סיומת .bat כיום, אנשים רבים משתמשים בסיומת .cmd כדי לשמור את הסקריפטים הניתנים להפעלה שלהם.

### מפרט פורמט CMD

ההתחלה של הכותרת מכילה את רשימת הקבוצות הקיימות בקובץ יחד עם סוגיהן. ניתן להשתמש בכל סוג פעם אחת לכל היותר. סוגים אלה הם:

- קוד
- נתונים
- תוספת
- מחסנית
- משתמש 1
- משתמש 2
- משתמש 3
- משתמש 4
- קוד משותף

כמו כן, קידומת מקטע תוכנית ב-DOS, 256 הבתים הראשונים של קבוצת הנתונים הם אפס. הם יאוכלסו על ידי CP/M-86 עם עמוד האפס. אם אין קבוצת נתונים, 256 הבתים הראשונים של קבוצת הקוד ישמשו במקום זאת.
## דוגמה לקובץ CMD
להלן דוגמה של סקריפט CMD להצגת מידע מערכות.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## הפניות

* [כיצד לכתוב סקריפט CMD](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [קובץ CMD (CP/M) - מאת ויקיפדיה](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

