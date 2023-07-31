{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - Report Definition Language-side Client",
  "keywords" :[ "rdlc", "שפת הגדרת דוח", "פורמט mkv", "XSD", "צד הלקוח של שפת הגדרת הדוח"],
  "description":"למד על פורמט קובץ RDLC שהוא ייצוג XML של הגדרת דוח SQL Server Reporting Services.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## מהו קובץ RDLC? ##

ה-RDLC מייצג Report Definition Language Client side. למעשה זוהי הרחבה של קובץ דוח שנוצר באמצעות טכנולוגיית דיווח של Microsoft. גרסת SQL Server 2005 של Report Designer משמשת ליצירת קבצים אלה. בקרת **ReportViewer** בצד הלקוח יכולה לבצע ישירות את דוחות ה-RDLC.

## קבצי RDL VS RDLC
קבצי |.rdl | קבצי .rdlc|
---|---|
|קבצי RDL נוצרים על ידי גרסת SQL Server 2005 של Report Designer|קובצי RDLC נוצרים על ידי גרסת Visual Studio 2005 של Report Designer|
|הוא משמש ב-SQL Server Reporting Services|הוא משמש ב-Visual Studio|
|זהו דוח מרוחק|זהו דיווח מקומי|
|צריך מופע Reporting Services כדי להפעיל אותו|אין צורך במופע Reporting Services|

## יצירת קבצי הגדרת דוח לקוח (.rdlc).
הפקד ReportViewer משמש להפעלת קבצי הגדרת דוח לקוח (.rdlc) תוך שימוש ביכולת העיבוד המובנית של הפקד. הלקוח מדווח שאתה מפעיל במצב עיבוד מקומי ניתן ליצור בקלות בפרויקט היישום שלך. להלן הגישות ליצירת הדוח:

- השתמש ב**אשף הדוחות** כדי ליצור הגדרת דוח לקוח חדשה (.rdlc).

- צור קובץ חדש של הגדרת דוח לקוח (.rdlc) באמצעות Visual Studio.

- צור הגדרת דוח באופן פרוגרמטי.


אתה יכול להציג דוח בתצוגה מקדימה רק על ידי הפעלתו בפקד **ReportViewer**. שים לב שאתה יכול לפתוח ולערוך את הגדרת הדוח בכל עת, ולאחר מכן לבנות או לפרוס את היישום כדי לבדוק את התוצאות.

## הפניות ##

- [יצירת קבצי הגדרת דוח לקוח (.rdlc)](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

