{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "הרחבה", "קובץ", "פורמט קובץ", "סוג קובץ מסד נתונים", "פורמט קובץ מסד נתונים", "חבילת יישום שכבת נתונים" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ DACPAC וממשקי API שיכולים ליצור ולפתוח קובצי DACPAC.",
  "title" :"DACPAC - Data Tier AppliCation Package",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## מהו קובץ DACPAC?

קובץ עם סיומת .dacpac (המשמעות של Data Tier AppliCation Package) הוא קובץ מסד נתונים, שנוצר עם יישום שכבת הנתונים של Microsoft SQL Server, המכיל את מודל מסד הנתונים לייצוג של אובייקטי מסד נתונים. מכיוון שהוא מכיל את המודל המלא של מסד הנתונים, הוא משמש לשחזור מסד נתונים מהפרטים הזמינים במודל. קבצי DACPAC נמסרים בדרך כלל לצוותי פריסה להתקנה בחצרים של הלקוח כדי לשחזר מסד נתונים. אלה ניתן לפתוח עם
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## פורמט קובץ DACPAC - מידע נוסף

קבצי חבילת הנתונים DACPAC הם למעשה קובצי ZIP דחוסים המכילים מספר קבצי [XML](/he/web/xml/) המכילים מידע על מודל מסד הנתונים, כגון טבלאות ותצוגות, המשמשים לשחזור מסד נתונים. על מנת להציג את התוכן של קבצי DACPAC, שנה את שמם של הקבצים מ-.dacpac ל-[.zip](/he/compression/zip/) וחלץ את ארכיון ה-zip באמצעות כל כלי עזר לביטול דחיסה.

להלן מספר קבצים שנמצאים בתוך קובץ DACPAC.

* [Content_Types].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Origin.xml

* model.xml

יש לציין ש-DACPAC אינו מכיל DATA ואובייקטים אחרים ברמת השרת. הקובץ יכול להכיל את כל סוגי האובייקטים שעשויים להישמר בפרויקט SSDT.

## הפניות

* [אפליקציות שכבת נתונים - יתרונות](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [פריסת יישום שכבת נתונים - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [כיצד ליצור קובץ DACPAC?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

