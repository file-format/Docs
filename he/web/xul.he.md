{
  "date" : "2021-05-24",
  "keywords" :["xul", "קובץ", "הרחבה", "פורמט קובץ", "הרחבת קובץ", "שפת ממשק משתמש XML"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - XML User Interface Language File",
  "description":"למד על פורמט קובץ XUL וממשקי API שיכולים ליצור ולפתוח קובצי XUL.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## מהו קובץ XUL?

קובץ עם סיומת .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) מייצג XML User Interface Language) הוא קובץ שפת סימון מבוסס [XML](/he/web/xml/) עבור יצירת ממשקי משתמש. זה פותח על ידי Mozilla עבור מפתחים כדי ליצור אלמנטים של ממשק משתמש גרפי הדומים לשפות סימון אחרות המשמשות ליצירת דפי אינטרנט. XUL נמצא בשימוש נרחב על ידי מוזילה בדפדפן פיירפוקס שבו השתמשה בבסיס הקוד של מוזילה. עיבוד XUL מתבצע באמצעות
[מנוע שממית](https://en.wikipedia.org/wiki/Gecko_(software)). מזלגות Firefox כגון Pale Moon, Basilisk ו-Waterfox שומרים על תמיכה בתוספות XUL. קובצי XUL מזוהים עם סוג MIME: application/vnd.mozilla.xul+xml.

## פורמט קובץ XUL

קובצי XUL נכתבים בטקסט רגיל המבוסס על פורמט קובץ XML ומעובדים באמצעות מנוע Gecko. שלושת החלקים העיקריים של מבנה XUL הם:

* `תוכן` - זה כולל את ההצהרות של החלון ורכיבי ממשק המשתמש הכלולים בהם.
* 'עור' - זה כולל כל גיליונות סגנון, תמונות וקבצים אחרים הקשורים לנושא. המראה של חלון מתואר בגיליונות הסגנונות.
* `מקומי` - טקסט המוצג בתוך חלון מאוחסן בנפרד ומשתמשים יכולים להשתמש במספר קבצי שפה.

### XUL דוגמה

הדוגמה הבאה יוצרת שלושה לחצנים הנערמים זה על גבי זה בכיוון אנכי.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## הפניות

* [XUL - מאת ויקיפדיה](https://en.wikipedia.org/wiki/XUL)
* [תיעוד XUL בארכיון - מאת מוזילה](https://wiki.mozilla.org/XUL:Home_Page)

