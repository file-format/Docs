{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ OSR וממשקי API שיכולים ליצור ולפתוח קובצי OSR.",
  "title" : "קובץ OSR - osu! הפעל מחדש את פורמט הקובץ",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-he",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## מהו קובץ OSR?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**סוג MIME של פורמט קובץ OSR:** x-osu-replay

## פורמט קובץ OSR

קבצי OSR נשמרים כקבצים בינאריים עם שדות נתונים קבועים כמו גם באורך משתנה.

|סוג נתונים| פורמט|
---|---|
|Byte |מצב משחק של השידור החוזר (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|מספר שלם |גרסת המשחק כאשר השידור החוזר נוצר (לדוגמה 20131216)|
|מחרוזת |osu! hash beatmap MD5|
|מחרוזת| שם שחקן|
|מחרוזת| אוסו! הפעל מחדש MD5 hash (כולל מאפיינים מסוימים של השידור החוזר)|
|קצר| מספר 300 |
|קצר| מספר 100 בסטנדרט, 150 בטאיקו, 100 ב-CTB, 100 במאניה|
|קצר| מספר 50 בסטנדרט, פרי קטן ב-CTB, 50 במאניה|
|קצר| מספר Gekis בסטנדרט, מקסימום 300s במאניה|
|קצר| מספר קאטוס בסטנדרט, 200 במאניה|
|קצר| מספר החמצות|
|מספר שלם| הציון הכולל המוצג בדוח הניקוד|
|קצר| השילוב הטוב ביותר המוצג בדוח הניקוד|
|בייט| שילוב מושלם/מלא (1 = ללא החמצות וללא הפסקות סליידר וללא סליידרים שהסתיימו מוקדם)|
|מספר שלם| נעשה שימוש במודים. ראה להלן רשימה של ערכי מוד.|
|מחרוזת| גרף עמודות חיים: זוגות מופרדים בפסיק u/v, כאשר u הוא הזמן באלפיות שניות לתוך השיר ו-v הוא ערך נקודה צפה מ-0 - 1 המייצג את כמות החיים שיש לך בזמן הנתון (0 = סרגל החיים הוא ריק, 1= סרגל החיים מלא)|
|ארוך| חותמת זמן (חלונות מתקתקים)|
|מספר שלם| אורך בבתים של נתוני הפעלה חוזרת דחוסים|
|Byte |נתוני הפעלה חוזרת דחוסה של מערך|
|ארוך| מזהה ציון מקוון|
|כפול| מידע נוסף על מוד. קיים רק אם תרגול יעד מופעל.|

## הפניות

* [OSU! משחק קצב](https://osu.ppy.sh/home)

* [פורמט קובץ OSR](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


