{
  "date" : "2022-04-01",
  "keywords" :[ "קובץ nkit", "פורמט קובץ nkit", "מהו קובץ nkit", "קובץ", "דוגמה של nkit", "סיומת קובץ nkit","הרחבה", "פורמט", "תחתונה של nkit", "קובץ פורמט של nkit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"למד על פורמט קובץ NKIT וממשקי API שיכולים ליצור ולפתוח קבצי NKIT.",
  "title" :"NKIT - פורמט קובץ תמונת דיסק",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## מהו קובץ NKIT?

קובץ NKIT הוא תמונת דיסק של נתונים שחולצו ממשחקי NintendoWii ו-GameCube. NKIT מיועד לפורמט Nintendo Toolkit. קובץ הדחיסה [ISO](/he/compression/iso/) המתקבל מנצל את הנתונים העיקריים של המשחקים הללו כדי להפעיל עם תוכניות אמולטור כגון Dolphin, Swiss ו-Nintendont. NKit מגיע בפורמטים של קבצים גולמיים (iso) ו-דחוסים (gcz), שניהם עוצבו תוך שמירה על יכולת השמעה וגודל התצוגה.

## פורמט קובץ NKIT

פורמט קובץ NKit הוא פורמט שאינו מאבד ומשמש לכווץ ושחזור תמונות Nintendo Wii ו-GameCube. הפורמטים זמינים בפורמטים של קבצי ISO ו-GCZ עבור כל אחד ממשחקי GameCube ו-Wii.

|מערכת |פורמט |חומרה נתמכת |דולפין נתמך |שחזור 1:1 |הערות|
---|---|---|---|---|---|
|GameCube| nkit.iso| כן |כן| כן |זהה ל-GameCube iso הדחוס|
|GameCube| nkit.gcz| לא| כן| כן |GCZ הוא פורמט הדחיסה הניתנת לחיפוש בלוק משל Dolphin|
|Wii| nkit.iso| לא כן| כן| פורמט RVT-H ניתן להשמעה רק בדולפין|
|Wii| nkit.gcz| לא כן| כן| RVT-H ב-GCZ ניתן לשחק בדולפין בלבד|

### כותרת NKIT

כותרת פורמט הקובץ NKIT היא כדלקמן.

|היסט |אורך |שם|
---|---|---|
|0x200 |0x4 |כותרת NKit 'NKIT'|
|0x204 |0x4 |NKit גרסה ' v01'|
|0x208 |0x4 |תמונת מקור מקורית CRC32|
|0x20C |0x4 |NKit CRC - גורם לקובץ NKit CRC32 להיות שווה למקור CRC ב-0x208 (ב-0x4 ב-GCZ)|
|0x210 |0x4 |אורך תמונת מקור|
|0x214 |0x4 |זיהוי זבל כפוי (כאשר מזהה דיסק שונה - נדיר - GameCube בלבד)|
|0x218 |0x4 |Wii Update מחיצה CRC32 אם הוסרה בעת ההמרה|

## הפניות ##

* [פורמט קובץ NKIT - מאת gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

