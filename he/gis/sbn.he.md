{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SBN - ESRI Spatial Index Binary File",
  "description":"למד על פורמט קובץ SBN וממשקי API שיכולים ליצור ולפתוח קובצי SBN.",
  "linktitle" : "SBN",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## מהו קובץ SBN?

קובץ עם סיומת .sbn הוא קובץ אינדקס מרחבי המשוייך לקובץ ESRI ArcGIS [.shp](/he/gis/shp/). הוא משמש לאופטימיזציה של שאילתות מרחביות כאשר בוצע אינדקס על הנתונים. סוג הקובץ השני המשמש לצד .sbn הוא קובץ .sbx. קבצי SBN ו-SBX מרכיבים יחד אינדקס צורות כדי להאיץ שאילתות מרחביות. קבצי SBN הם אופציונליים וניתן לפתוח אותם באמצעות [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview).

## פורמט קובץ SBN - מידע נוסף

קובצי SBN מאוחסנים בדיסק כקבצים בינאריים ופרטי פורמט הקובץ הפנימי שלהם אינם זמינים. אלה מאחסנים את הייצוג הבינארי של קובץ SHP עבור שאילתות מרחביות. קובץ האינדקס SBX משמש לצד קבצי SBN להאצת השאילתות המרחביות בקבצי shape.

## הפניות

* [תיאור טכני של ESRI ShapeFile](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf)
* [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview)

