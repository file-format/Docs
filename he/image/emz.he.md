{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ emz", "פורמט קובץ emz", "מהו קובץ emz", "קובץ", "דוגמה ל-emz", "סיומת קובץ emz","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ EMZ - קובץ מטא משופר דחוס של Windows",
  "description":"למד על פורמט קובץ EMZ וממשקי API שיכולים ליצור ולפתוח קובצי EMZ.",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## מהו קובץ EMZ?

קובץ עם סיומת .emz הוא מיכל דחוס של Enhanced Metafile (קובץ [EMF](/he/image/emf/)). אלה נדחסים באמצעות טכניקת הדחיסה [GZIP](/he/compression/gz/) שהיא שיטת הדחיסה הנפוצה במערכות הפעלה UNIX ו-LINUX. בטל קישור של ZIP (/he/compression/zip/), GZIP דוחס את הארכיון בכללותו במקום לדחוס קבצים בודדים. קבצי EMZ קטנים יותר בהשוואה לקבצי EMF ומסייעים בהעברה מהירה במהלך שיתוף קבצים מקוון. חלק מהיישומים שיכולים לפתוח קבצי EMZ כוללים את Microsoft Visio 2019, Microsoft Office 2019, XnView MP ו- File Viewer Plus.

## פורמט קובץ EMZ

קובצי EMZ הם [Gzip](/he/compression/gz/) דחוסים ומכילים בתוכם [EMF](/he/image/emf/). Gzip משתמש באלגוריתם DEFLATE עבור דחיסה של הארכיון ושונה ביישום דחיסה. ניתן לפרק קובץ EMZ באמצעות כלי עזר לדחיסת GZip כגון GNU Zip. פורמט הקובץ מורכב מ:

* כותרת הקובץ
* כותרות אופציונליות
* נתונים דחוסים
* כותרת תחתונה של קובץ

פורמט הקובץ GZIP [מפרט גרסה 4.3](http://tools.ietf.org/html/rfc1952) שפורסם על ידי Internet Engineering Task Force (IETF) מכיל מידע מפורט על פורמט הקובץ.

## הפניות

* [RFC1952: מפרט פורמט קובץ GZIP](http://tools.ietf.org/html/rfc1952), מאת [IETF](https://www.ietf.org/)
* [Windows MetaFile - ויקיפדיה](https://en.wikipedia.org/wiki/Windows_Metafile)

