{
  "date" : "2021-07-28",
  "keywords" :[ "קובץ ntf", "פורמט קובץ ntf", "מהו קובץ ntf", "קובץ", "דוגמה ל-ntf", "סיומת קובץ ntf","סיומת", "פורמט" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - קבצים בפורמט העברה לאומי",
  "description":"למד על פורמט קובץ NTF וממשקי API שיכולים ליצור ולפתוח קובצי NTF.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## מהו קובץ NTF?
הקבצים עם סיומת .ntf נקראים **National Transfer Format (NTF)** קבצים; משמש בעיקר על ידי סקר חיל האוויר הבריטי (OS); במיוחד להעברת נתונים גיאו-מרחביים. הוא מנוהל על ידי מכון התקנים הבריטי. זה הפך לפורמט ההעברה הסטנדרטי לנתונים דיגיטליים של סקר Ordnance. הקרנת ה-National Grid של בריטניה, שהיא סוג של Transverse Mercator, מכילה את כל המידע ב-Georeferences עבור קבצי NTF.

## פורמט קובץ NTF
פורמט הקובץ NTF הוא בבעלות Ordnance Survey בבריטניה; נתמך על ידי ספריית GDB לייבוא. הגרסה הנוכחית של פורמט הקובץ NTF היא 2.0. פורמט קובץ זה הוצג כדי לתת מענה למגבלה של קטע וקטור **PCIDSK** שיש לו רק שדה תכונה אחד לכל מבנה, אך יש מגוון של תכונות שניתן לחלץ עם נתונים וקטוריים. כדי לעקוף את פורמט הקובץ NTF מורכב כבעל שני מקטעים. כל קטע מורכב מאותם וקטורים, אבל עם תכונות שונות. הפלח הראשון של קובץ וקטור NTF מכיל את הוקטורים עם מספר קוד התכונה בתור התכונה. הקטע השני מכיל את הוקטורים עם הערך בתור התכונה.

### מערכת הפניה לקואורדינטות
ספריית GDB מייצגת נתוני רסטר וויקטור עם מאפייני הקרנת TM המתאימים:

- קו אורך ייחוס: 49.0
- קו רוחב ייחוס: 2.0
- איסת שווא: 400000
- צפון שקר: -100000
- קנה מידה: 0.9996012717
- אליפסואיד: Airy 1830 (E009)
אין תמיכה זמינה לעדכון, או כתיבת קובצי NTF, וגם לא ניתן לקשר את קבצי ה-DTM.

### דוגמה של Ogrinfo
הדוגמה הבאה משתמשת ב-**ogrinfo** בקובץ NTF כדי לאחזר מספרי שכבות:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## הפניות

* [פורמט העברה לאומי של בריטניה (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [מיפוי אינטרנט - מאויר על ידי טיילר מיטשל](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

