{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "קובץ MPK - פורמט קובץ חבילת מפת ArcGIS",
  "description":"למד על פורמט קובץ MPK וממשקי API שיכולים ליצור ולפתוח קובצי MPK.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-he",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## מהו קובץ MPK?

קובץ MPK הוא קובץ חבילת ArcGIS Map שנוצר עם ArcGIS. הוא מכיל מסמך מפה .mxd ונתונים קשורים. בנוסף, הוא מכיל מידע נוסף כגון שכבות עם הפניות, סמלים ומשאבים אחרים. קובץ MPK משמש לשיתוף מפות ונתונים עם משתמשים אחרים. זה מבטל את הזמינות של אחרים בעלי מקור הנתונים המקורי וגם עוזר להפיץ מפות לשימוש במכשיר נייד.

## פורמט קובץ MPX

פרטי פורמט הקובץ הפנימי של קובצי MPX אינם זמינים לציבור לעיונם של המפתח.

### צור קובץ MPK באמצעות ArcGIS

ניתן ליצור קבצי MPK באמצעות ArcGIS. ניתן להשתמש באפשרות שתף בשם בתפריט חבילת מפה ליצירת קובץ .mpk המכיל את מסמך המפה ואת כל הנתונים והמשאבים שלו. לאחר מכן ניתן לשתף קובץ MPK זה עם אחרים וניתן לפתוח אותו ב-ArcMap וב-ArcGIS Pro כדי להציג את המפה והנתונים.

### צור קובץ MPK באמצעות Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### שימוש ב-Python ליצירת חבילות מפה עבור כל מסמכי המפה בתיקייה

קוד Python הבא מוצא ויוצר חבילות מפה עבור כל מסמכי המפה השוכנים בתיקייה שצוינה.

```
# Name: PackageMap.py
# Description:  Find all the map documents that reside in a specified folder and create map packages for each map document.

# import system modules
import os
import arcpy

# Set environment settings
arcpy.env.overwriteOutput = True
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing"

# Loop through the workspace, find all the mxds and create a map package using the same name as the mxd
for mxd in arcpy.ListFiles("*.mxd"):
    print ("Packaging: {0}".format(mxd))
    arcpy.PackageMap_management(mxd, os.path.splitext(mxd)[0] + '.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```

## הפניות

* [מפת חבילה](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


