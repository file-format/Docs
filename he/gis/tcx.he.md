{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ TCX- קובץ XML של מרכז ההדרכה",
  "description":"למד על פורמט קובץ TCX וממשקי API שיכולים ליצור ולפתוח קובצי TCX.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## מהו קובץ TCX?

קובץ TCX (מרכז הדרכה XML) הוא פורמט לחילופי נתונים המשמש לשיתוף נתונים בין מכשירי כושר. הוא הוצג בשנת 2008 עם מוצר ה-Training Center של Garmin. נתוני אימון כגון דופק, קצב ריצה, קצב אופניים, קלוריות וזמן הקפה מאוחסנים בפורמט [XML](/he/web/xml/) בתוך קובץ TCX. בנוסף, נתוני סיכום על מסלול האימון כלולים גם הם בקובץ TCX. קבצי TCX דומים לקבצי [FIT](/he/gis/fit/) שנוצרו עם מכשירי ספורט לבישים של Garmin.

## פורמט קובץ TCX - מידע נוסף

קובצי TCX נשמרים בתקליטור כקובצי XML כאשר כל רשומה נשמרת כפעילות. פעילות כוללת את כל הנתונים של אימון, כגון זמן, זמן הקפה, מזהה, דופק, אינטנסיביות, קצב ומידע על מסלול המכיל את זוגות המיקום יחד עם חותמת הזמן עבור אותו מיקום רוחב-ארוך בדומה ל-[GPX] (/he/gis/gpx/) קבצים.

### גרסאות פורמט קובץ TCX

ישנן שתי גרסאות של פורמט זה עם סכימות XML משלהן המתארחות על ידי Garmin. להלן כמה מהם:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## פרוטוקול נתונים TCX

גרסה מהירה של פורמט TCX XML זמינה ב-Github בשם [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## הפניות ##

* [XML של מרכז הדרכה](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

