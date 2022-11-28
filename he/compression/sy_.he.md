{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ SY_ - קובץ SYS דחוס",
  "description":"למד על פורמט קובץ SY_ וממשקי API שיכולים ליצור ולפתוח קבצי SY_.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## מהו קובץ SY_?

קובץ SY_ הוא קובץ .sys דחוס המשמש את מתקיני התוכנה כדי להקטין את גודל קובצי ההתקנה הארוזים בתוך תוכנית ההתקנה. זה מקטין את הגודל הכולל של המתקין. ניתן להרחיב קבצי SY_ באמצעות כלי השירות של שורת הפקודה Expand של Microsoft שמרחיבה קובץ דחוס אחד או יותר.

## SY_ פורמט קובץ - מידע נוסף

קבצי SY_ נשמרים בדיסק כקבצים בינאריים דחוסים. עם זאת, פורמט הקובץ הפנימי שלהם אינו זמין לציבור. כלי השירות Microsoft Expand שורת הפקודה יכול להרחיב קבצי SY_ באמצעות אחת משורות הפקודה הבאות.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
בהרחבה, קובצי SY_ מומרים לקובץ [SYS](https://docs.fileformat.com/system/sys/).

קבצי SY_ דומים לקבצי EX_ ו-DL_.

## הפניות

* [StuffIt - מאת ויקיפדיה](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

