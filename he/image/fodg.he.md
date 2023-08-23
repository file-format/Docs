{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ fodg", "פורמט קובץ fodg", "מהו קובץ fodg", "קובץ", "דוגמה של fodg", "סיומת קובץ fodg","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - OpenDocument Drawing File Format",
  "description":"למד על פורמט קובץ FODG וממשקי API שיכולים ליצור ולפתוח קבצי FODG.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ FODG?

קובץ עם סיומת .fodg הוא פורמט קובץ Apache OpenOffice Drawing לאחסון רכיבי ציור. הוא מבוסס על מפרטי פורמט הקובץ המתוארים על ידי Advancement of Structural Information Standards (OASIS). פורמט קובץ דומה נוסף עבור גרפיקה של OpenOffice הוא [ODG](/he/image/odg/) המאחסן רכיבי ציור כתמונה וקטורית. ניתן לפתוח קבצי FODG עם OpenOffice כמו גם עם LibreOffice. פורמטים אחרים של קבצים הנתמכים על ידי OpenOffice, למשל, כוללים [ODT](/he/word-processing/odt/), ODF, [ODP](/he/presentation/odp/) ו-[ODS](/he/spreadsheet/ods/).

## פורמט קובץ FODG

FODG מבוסס על פורמט קובץ ה-XML של OpenDocument התואם את OASIS OpenDocument Format ISO/IEC 26300. יש לו Internet Media Type application/vnd.oasis.opendocument.graphics וגם תואם org.oasis-open.opendocument public.composite-content . מבנה ה-XML משותף לכל סוגי המסמכים כגון גיליון אלקטרוני, קבצי ציור ומסמכי טקסט. מסמכי OpenOffice מנצלים את ההפרדה בין חששות על ידי הפרדת התוכן, הסגנונות, המטא נתונים והגדרות היישום לארבעה קובצי XML נפרדים.

`<office:document-content>` - תוכן מסמך וסגנונות אוטומטיים המשמשים בתוכן.
`<office:document-styles>` - סגנונות המשמשים בתוכן המסמך וסגנונות אוטומטיים המשמשים בסגנונות עצמם.
`<office:document-meta>` - מסמך מטא מידע, כגון המחבר או שעת פעולת השמירה האחרונה.
`<office:document-settings>` - הגדרות ספציפיות ליישום, כגון גודל החלון או מידע המדפסת.

## הפניות ##
* [מפרט עתידי עבור סטנדרטיזציה של גרסה 1.3 ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [OASIS Open Document Format עבור יישומי Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [פורמט OpenDocument - ויקיפדיה](https://en.wikipedia.org/wiki/OpenDocument)

