{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ CPG - קובץ דף קוד ESRI",
  "description":"למד על פורמט קובץ CPG וממשקי API שיכולים ליצור ולפתוח קובצי CPG.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## מהו קובץ CPG?

קובץ CPG הוא קובץ אופציונלי הנדרש ב-ESRI Shapefile המשמש לציון דף הקוד לזיהוי ערכת התווים שיש להשתמש בה. אלה מאוחסנים בפורמט קובץ טקסט רגיל ומכילים מידע על הקידוד שהוחל ליצירת קובץ הצורה. במקרה שקובץ CPG אינו זמין, קובץ הצורה משתמש בקידוד ברירת המחדל של המערכת. קובץ CPG, אם קיים, חייב להיות בעל קידומת זהה לזה של קובץ [SHP](/he/gis/shp/), למשל, roads.shp, roads.cpg.

ניתן לפתוח קבצי CPG עם ESRI ArcGIS Pro.

### פורמט קובץ CPG - מידע נוסף

בעת הצגת קובץ shape ב- ArcCatalog או כל יישום אחר של ArcGIS, אתה רואה רק את קובץ הצורה. אבל במציאות, shapefile משתמש בקבצים משויכים אחרים הנקראים לצד קובץ הצורה הראשי. קובץ ה-CPG הוא גם אחד מאלה אם הוא קיים לצד קובץ ה-SHP הראשי.

## הפניות

* [סיומות קובץ Shapefile
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

