{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "קובץ", "הרחבה", "פורמט קובץ", "אקסל", "גיליון אלקטרוני" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ OTS וממשקי API שיכולים ליצור ולפתוח קובצי OTS.",
  "title" :"OTS - פורמט קובץ תבנית גיליון אלקטרוני של OpenDocument",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## מהו קובץ OTS?

קובץ עם סיומת .ots הוא קובץ OpenDocument Spreadsheet Template שנוצר עם תוכנת היישום Calc הכלולה ב- Apache OpenOffice. תוכנת היישום Calc דומה לאקסל הזמינה ב-Microsoft Office. פורמט קובץ OTS משמש ליצירת תבניות המכילות הגדרות מוגדרות מראש הקשורות לסגנונות, גופן, נתונים, פריסת גיליון אלקטרוני ועיצוב. לקבצי OTF יש 'יישום מסוג mime/vnd.oasis.opendocument.spreadsheet-template'. קובצי תבניות אלה יכולים לשמש כנקודת התחלה ליצירה ולשמירה של קבצי נתונים בפועל שנשמרים ב[פורמט קובץ ODS](/he/spreadsheet/ods/). ניתן להשתמש בקבצי OTS עם יישומים כגון OpenOffice ו-LibreOffice.

## פורמט קובץ OTS

קובצי OTS נשמרים בפורמט קובץ מבוסס XML של OASIS OpenDocument המורכב מאוסף של מספר מסמכי משנה עם חבילה כארכיון [ZIP](/he/compression/zip/). כל ארכיון zip מאחסן חלק מהמסמך המלא וכל מסמך משנה מאחסן היבט מסוים של המסמך. לדוגמה, מסמך משנה אחד מכיל את מידע הסגנון ומסמך משנה אחר מכיל את תוכן המסמך. מסמך ODF טיפוסי כולל את הרכיבים הבאים:

### OTS Content.xml

קובץ content.xml מכיל את התוכן בפועל של המסמך. עם זאת, זה לא כולל נתונים בינאריים כגון תמונות.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml של פורמט קובץ OTS

הקובץ styles.xml מכיל מידע עיצובי ונמצא בשימוש רב לעיצוב ולפריסה. סוגי הסגנונות כוללים:

* סגנונות פסקה
* סגנונות דפים
* סגנונות אופי
* סגנונות מסגרת
* רשימת סגנונות

### Meta.xml

קובץ meta.xml מכיל מידע על מטא-נתונים של הקובץ כגון מחבר, תאריך שינוי אחרון וכו'.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

הקובץ `settings.xml` כולל הגדרות ברמת המסמך כגון מקדם זום ומיקום הסמן.

## הפניות ##

* [מפרט OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - מאת ויקיפדיה](https://en.wikipedia.org/wiki/OpenDocument)

