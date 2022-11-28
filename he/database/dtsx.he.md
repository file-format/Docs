{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "הרחבה", "קובץ", "פורמט קובץ", "סוג קובץ מסד נתונים", "פורמט קובץ מסד נתונים", "קבצי מסד נתונים" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ DTSX וממשקי API שיכולים ליצור ולפתוח קובצי DTSX.",
  "title" :"פורמט קובץ DTSX - קובץ הגדרות DTS של SQL Server",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## מהו קובץ DTSX?

קובץ עם סיומת .dtsx (Data Transformation Services Package XML) הוא קובץ Data Transformation Services (DTS) המשמש את Microsoft SQL להתייחסות לשלבים/כללים של העברת נתונים להעברת נתונים ממסד נתונים אחד למשנהו. זה כולל את הטרנספורמציות וכל שלבי עיבוד אופציונליים שעשויים להידרש במהלך העברת הנתונים בין נקודת המוצא והיעד. SQL Server Integration Services (SSIS), רכיב של Microsoft SQL Server, משתמש בקבצי DTSX כדי לזהות את השלבים לעיבוד נתונים בין שרתי מסד נתונים. ניתן לפתוח קבצי DTSX עם Microsoft SQL Server 2019.

## פורמט קובץ DTSX

העברת נתונים בין שרתי מסד נתונים דורשת כללים ושלבי עיבוד כדי להבטיח את שלמות הנתונים במהלך פעולה זו. SSIS מבטיח שכל הפעילויות הללו, כדי להעביר ולהתאים נתונים ממקורות שונים בארגון, מתרחשות בצורה נוחה. זה המקום שבו מגיע DTSX שמגדיר את המבנים שישמשו את SSIS כדי לקבוע את השלבים שבהם ניתן לעבד את הנתונים כפי שהם עוקבים בשלבים אלה.

זרימת הנתונים המתוארת על ידי DTSX היא כפי שמוצג בתמונה הבאה.

{{< figure src="../DataFlowDTSX.png" alt="זרימת נתונים DTSX" >}}

DTSX מבוסס על [XML](/he/web/xml/) ומתועד ב-[MS-DTSX](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13- 4b5b-a388-aa3c65aec1dd). ה-Refactoring המשופר של DTSX XML הוא DTSX 2.0 הכולל תכונות חדשות למבנים, החלפה של מאפיינים בעלי שם כתכונות XML אב, מציין ברירות מחדל עבור רוב ערכי התכונות ומיקום של רכיבים חוזרים בתוך אלמנט אב. מבני DTSX מתוארים באמצעות [סכימות XML](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) והוא הפורמט המבנה XML של טקסט סלולרי.

## הפניות

* [פורמט DTSX - Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [פורמט DTSX 2 - מאת Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

