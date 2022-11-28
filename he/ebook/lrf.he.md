{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "קובץ", "הרחבה", "פורמט", "ספר אלקטרוני", "ספר דיגיטלי" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ LRF וממשקי API שיכולים ליצור ולפתוח קובצי LRF.",
  "title" :"פורמט קובץ LRF - קובץ קורא נייד של Sony",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## מהו קובץ LRF?

קובץ עם סיומת .lrf הוא קובץ Broad Band eBook (BBeB) המכיל נתונים עבור Sony BBeB, כולל טקסט, תמונות ונתוני עימוד. הקובץ נשמר בפורמט בינארי דחוס המכיל כותרת עליונה, מספר מוגדר של אובייקטים ואינדקס אובייקטים. קובצי LRF ו-LRX כוללים את שני פורמטים הזמינים של ספרי BBeB. קובצי ה-LRF אינם מוצפנים וניתן להרכיב אותם מקבצי [LRX](/he/ebook/lrf/). ניתן להמיר את קבצי ה-LRF מכמה סוגי קבצים אחרים כולל PDF ו-HTML. אם המחשב שלך לא יכול לפתוח את קובץ LRF, כנראה שלא התקנת את התוכנה כדי לפתוח או לערוך את קבצי LRF. תוכניות שיכולות לפתוח קבצי LRF הן Caliber, BookDesigner, Makelrf ו-Canon Book Creator עבור Windows, Caliber עבור Linux, Caliber ו-Sony Reader עבור Macintosh.

## היסטוריה קצרה

סוג קובץ LRF משויך בראש ובראשונה ל-Line Rider על ידי [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). רוכב השורה הוא צעצוע לפיזיקה אינטרנטית, והוא הומצא בספטמבר 2006 על ידי סטודנט באוניברסיטה סלובנית, Boštjan Čadež. eBook eReaders של מותג Sony (כגון קוראי Sony PRS-500 ו-Sony Librie) משתמשים בסיומת הקובץ LRF עבור המסמכים והטקסטים שלהם. סוג קובץ קנייני זה מיושן כעת, כמו גם קבצי LRS ו-LRX הקשורים. שלושת סוגי הקבצים הללו הרכיבו את BroadBand eBook (BBeB) אשר הופסק בשנת 2010 כאשר סוני החלה למכור את הספרים האלקטרוניים שלהם בפורמט EPUB.

## פורמט קובץ LRF

מפרטים מפורטים של פורמט קובץ LRF זמינים ב-[ארכיון אינטרנט](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). קובץ LRF מורכב מ:
*כותרת
* מספר חפצים
* אינדקס אובייקט.

כל הערכים האלה הם בסדר של Intel (LSB ראשון).

### כותרת LRF

|היסט (hex) |גודל (בתים) |שם/משמעות| ערך לדוגמה|
---|---|---|---|
|0 |8| חתימת LRF| 4C 00 52 00 46 00 00 00 = "LRF" ב-Unicode|
|8 |2| גרסה?| 999 ברוב הקבצים|
|A |2| "Psuedo-Encryption" |בייט מפתח 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| NumberOfObjects |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| לא ידוע | 0|
|24 |1| דגלים| (16 - אחורה מקדימה, 1 = מלפנים לאחור) 16|
|25 |1| לא ידוע |(ריפוד?) 0|
|26 |2| לא ידוע | 1600|
|28 |2| לא ידוע | (ריפוד?) 0|
|2A |2| גובה?| 600|
|2C |2| רוחב?| 800|
|2E |1| לא ידוע | 24|
|2F |1| לא ידוע |(ריפוד?) 0|
|30 |0x14| לא ידוע | אפסים|
|44 |4| מזהה אובייקט של אובייקט PlaneStream (0x1E) בלבד| 0x0042|
|48 |4| לא ידוע |0x1536|
|4C |2| XMLCompSize| 0x035C|


## הפניות

* [פורמט קובץ LRF](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - מאת ויקיפדיה](https://en.wikipedia.org/wiki/BBeB)

