{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SSF - Trimble Standard Storage Format File",
  "description":"למד על פורמט קובץ SSF וממשקי API שיכולים ליצור ולפתוח קובצי SSF.",
  "linktitle" : "SSF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-24"
}

## מהו קובץ SSF?

קובץ עם קובץ ssf הוא פורמט קובץ אחסון נתונים Geospatial המשמש את יישומי תוכנת ה-GIS Navigation [Trimble](https://www.trimble.com). הוא מאחסן נתוני GPS שנרשמו מהשדה באמצעות התקני Trimble. יומן ה-GPS מיובא לאחר מכן באחד מהיישומים של חבילת היישומים של Trimble. יומן ה-GPS הכלול ב-SSF משמש ליצירת מערכות קואורדינטות מותאמות אישית. ניתן לפתוח קובצי SSF עם [Trimble Navigation GPS Pathfinder Office](https://geospatial.trimble.com/products-and-solutions/ssf-and-ddf-data-format-extensions-fme), Trimble Navigation GPS Pathfinder Tools SDK ו-ESRI ArcGIS למחשב שולחני עם תוסף Trimble GPS Analyst.

## פורמט קובץ SSF - מידע נוסף

כאשר נתוני GPS מועברים ממכשיר Trimble למחשב לצורך עיבוד אחר, כל הקבצים הללו משולבים יחד לקובץ ssf יחיד. הקובץ הגולמי הלא מעובד הזה משמש את תוכנת העיבוד לאחר ביצוע תיקונים וסיוע בניהול נתונים.

קובצי SSF מאוחסנים על דיסק כפורמט קובץ קנייני של Trimble ומפרטי הפרטים שלו אינם זמינים לציבור. זה ספציפי למכשירי Trimble ומייצג נתונים של יחידת ה-GPS. עד כה, אין פתרון חינמי לא מסחרי זמין לקריאה או המרת קבצי SSF.

## הפניות

* [מהדורת חדשות של טרימבל](https://www.trimble.com/news/release.aspx?id=050510b)

