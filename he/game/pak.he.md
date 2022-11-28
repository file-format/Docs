{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "פורמט קובץ", "מהו קובץ pak", "קובץ", "דוגמה פאק", "קובץ חבילת משחק וידאו","הרחבה"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על קובץ .pak וממשקי API שיכולים ליצור ולפתוח קובצי PAK.",
  "title" :"פורמט קובץ PAK- קובץ חבילת משחק וידאו",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## מהו קובץ PAK?

קובץ PAK הוא קובץ חבילה שנוצר על ידי משחקי וידאו שונים לארכיון נתוני משחקים. בעיקרו של דבר, זה פורמט קובץ משחק. זה יכול לכלול רכיבי משחק מרובים כגון גרפיקה, טקסטורות, צלילים, אובייקטים, יחד עם נתוני משחק אחרים. הארכיון נשמר ברובו כקובץ .zip וניתן לחלץ אותו באמצעות תוכנות דחיסה פופולריות כגון WinZip ו-WinRAR. דוגמאות למשחקי וידאו המשתמשים בקובצי PAK כוללות Quake, Hexen, Crysis ו-Half-Life.

## פורמט קובץ PAK - מידע נוסף

ברוב המקרים, קבצי PAK נשמרים ב[פורמט קובץ ZIP](/he/compression/zip/). אבל יישומים שונים עשויים להשתמש בפורמט קובץ שונה לאחסון קבצים אלה.


## איך פותחים קבצי PAK?

אתה יכול לפתוח קבצי PAK עם יישומים כגון [PakExplorer](https://www.quaketerminus.com/tools.shtml) ו-[SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

***------------------------------------------------ -------------------------------------------------- -------------------------------

## פורמט קובץ PAK - Simutrans Object File

קובץ עם סיומת .pak הוא פורמט קובץ סימולציית תחבורה [Simutrans](https://www.simutrans.com/en/). הוא מכיל אובייקטים המשמשים בסימולציה כגון גרפיקה שנעשתה על ידי המשתמש ותוכן נתונים. זה יכול לכלול כמה אובייקטים שונים כגון רכבי משחק, בניינים, שטח וכו'. קבצי PAK נוצרים באמצעות MakeObject, כלי עזר שמרכיב קבצי .dat ותמונות .png ליצירת אובייקטי סימולציה אלה. Simutrans מאפשרת לשחקנים לנהל מערכת תחבורה מוצלחת על ידי בנייה וניהול של מערכות תחבורה לנוסעים, דואר וסחורות דרך היבשה

## כיצד ליצור קבצי PAK?

Simutrans מונה דוגמאות ליצירת קבצי PAK במערכות ההפעלה Windows ו-Linux.

### מערכת ההפעלה של Windows

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## הפניות

* https://simutrans-germany.com/wiki/wiki/en_doPak
* https://en.wikipedia.org/wiki/Simutrans

