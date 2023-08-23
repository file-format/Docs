{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ wmz", "פורמט קובץ wmz", "מהו קובץ wmz", "קובץ", "דוגמה ל-wmz", "סיומת קובץ wmz","סיומת", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ WMZ - Metafile Windows דחוס",
  "description":"למד על פורמט קובץ WMZ וממשקי API שיכולים ליצור ולפתוח קבצי WMZ.",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## מהו קובץ WMZ?

קובץ עם סיומת .wmz הוא גרסה דחוסה של [WMF](/he/image/wmf/) ומשמש לאחסון מטא-קבצים. זהו קובץ ברמה בינונית שנוצר על ידי גרסאות ישנות יותר של יישומי Microsoft Office והוא אינו בשימוש פופולרי במיוחד. קבצי WMZ נוצרים תוך כדי שמירת מסמכים בפורמט [HTML](/he/web/html/). אלה עשויים להיווצר גם בעת שליחת דואר אלקטרוני של מסמכים המכילים קליפ ארט, משוואות וכו'. יישומים שיכולים לפתוח קבצי WMZ כוללים (אך לא רק) Corel Winzip ו-Apple Archive Utility.

## פורמט קובץ WMZ

קבצי WMZ הם [Gzip](/he/compression/gz/) דחוסים ומכילים בתוכם [WMF](/he/image/wmf/). Gzip משתמש באלגוריתם DEFLATE לדחיסה של הארכיון. GZIP שונה מפורמט הארכיון [ZIP](/he/compression/zip/) מכיוון שהוא מחיל אלגוריתם דחיסה להשלמת הארכיון ולא על הקבצים הבודדים. פורמט הקובץ מורכב מ:

* כותרת הקובץ
* כותרות אופציונליות
* נתונים דחוסים
* כותרת תחתונה של קובץ

פורמט הקובץ GZIP [מפרט גרסה 4.3](https://datatracker.ietf.org/doc/html/rfc1952) שפורסם על ידי Internet Engineering Task Force (IETF) מכיל מידע מפורט על פורמט הקובץ.

## הפניות

* [RFC1952: מפרט פורמט קובץ GZIP](https://datatracker.ietf.org/doc/html/rfc1952), מאת [IETF](https://www.ietf.org)
* [Windows MetaFile - ויקיפדיה](https://en.wikipedia.org/wiki/Windows_Metafile)

