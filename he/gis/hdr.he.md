{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ HDR- ESRI BIL Header File Format",
  "description":"מהו קובץ HDR?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## מהו קובץ HDR?

קובץ HDR הוא קובץ כותרת GIS המכיל מידע על כותרת עבור קובץ Band interleaved by line (.BIL). הוא מתאר את נתוני התמונה ויש לו שם זהה לזה של קובץ התמונה. קובץ HDR מורכב מקבוצה של ערכים, שכל אחד מהם מתאר תכונה מסוימת של התמונה. קובץ HDR מתאר את הפריסה והעיצוב של קובץ BIL לתרגום לקואורדינטות בעולם האמיתי בשילוב עם קובץ גיאוגרפיה נפרד.

## פורמט קובץ HDR

קובצי HDR נשמרים בפורמט קובץ טקסט ASCII. הוא מכיל קבוצה של ערכים כאשר כל ערך מתאר תכונה מסוימת של התמונה. לכל קובץ HDR יש את הפורמט הבא:

```
<keyword> <value>
```

`<keyword> ` - זה מציין את התכונה המסוימת שמוגדרת
`<value> ` - זהו הערך שאליו מוגדרת התכונה

אין הגבלה על סדר הערכים בכותרת. עם זאת, כל ערך חייב להיות בשורה נפרדת של השורה כדי להתאים לשיטת הניתוח המשמשת קוראי HDR.

## סיכום של מילות מפתח בשימוש בקובץ HDR

|מילת מפתח |ערך מקובל |ברירת מחדל|
---|---|---|
|מצמצם |כל מספר שלם > 0| אף אחד
|ncols |כל מספר שלם > 0| אף אחד
|nbands |כל מספר שלם > 0| 1
|nbits |1, 4, 8, 16, 32| 8
|סדר בתים| I = Intel;M = Motorola |זהה למחשב מארח|
|פריסה| bil, bip, bsq| bil|
|skipbytes| כל מספר שלם ≥ 0| 0
|ulxmap |כל מספר ממשי| 0|
|ulymap |כל מספר ממשי |מצומצם - 1|
|xdim |כל מספר ממשי| 1
|ידים |כל מספר ממשי| 1
|bandrowbytes |כל מספר שלם > 0| המספר השלם הקטן ביותר ≥ (ncols x nbits) / 8|
|totalrowbytes |כל מספר שלם > 0| עבור bil: nbands x bandrowbytes; עבור bip: המספר השלם הקטן ביותר ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes |כל מספר שלם ≥ 0| 0|

## הפניות

* [פורמט קובץ HRD - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

