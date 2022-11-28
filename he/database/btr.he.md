{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "סיומת", "קובץ", "פורמט קובץ", "סוג קובץ מסד נתונים", "פורמט קובץ מסד נתונים", "בסיס נתונים של Btrieve" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ BTR וממשקי API שיכולים ליצור ולפתוח קובצי BTR.",
  "title" :"BTR - Btrieve Database File",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## מהו קובץ BTR?

קובץ עם סיומת .btr הוא קובץ מסד נתונים שנוצר על ידי יישום מסד נתונים עסקה [Btrieve](https://www.actian.com/). בניגוד למערכות ניהול מסדי נתונים יחסיים (RBMS), Btrieve מבוססת על שיטת גישה רציפה באינדקס (ISAM), שהיא דרך לאחסן נתונים לאחזור מהיר. קובץ BTR מאחסן אוסף של רשומות ומשמש להפקת דוחות בהתאם לדרישות. ניתן לפתוח קבצי BTR באמצעות Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility ו- Legend Software BTRIEVE Viewer.

## מבנה קובץ BTR - מידע נוסף

מבנה הנתונים הפנימי והיישור של כל בייט במבנה של קובץ BTR אינם זמינים לציבור. עם זאת, Brieve
מספק את [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) שניתן להשתמש בו כדי לקרוא את המידע מקובצי BTR. זה תואם לשפות התכנות ולסביבות הפיתוח הבאות.

* Embarcadero C/C++
* Embarcadero Delphi
* GNU C/C++
* מיקרו פוקוס COBOL
* Microsoft Visual Basic
* Microsoft Visual C++
* ווטקום C/C++

אחזור נתונים מקובץ BTR תלוי בקובץ ה-DDF המשויך אליו. ללא ה-DDF, לא יהיה קל לשלוף את המידע מקובץ כזה.

## הפניות

* [Btrieve - ויקיפדיה](https://en.wikipedia.org/wiki/Btrieve)
* [מבוא לממשקי API של Btreive](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

