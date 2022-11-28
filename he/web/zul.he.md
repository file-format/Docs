{
  "date" : "2021-05-24",
  "keywords" :["זול", "קובץ", "הרחבה", "פורמט קובץ", "סיומת קובץ", "פתוח"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - ZK User Interface File",
  "description":"למד על פורמט קובץ ZUL וממשקי API שיכולים ליצור ולפתוח קבצי ZUL.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## מהו קובץ ZUL?

קובץ עם סיומת .zul הוא קובץ אינטרנט שנוצר עם שפת ה-User Interface Markup Language (ZUML) ומכיל הגדרות לרכיבי ממשק משתמש. מחלקות Ajax ו-Java תומכות בשימוש ב-ZUML המבוסס על [XML](/he/web/xml/) לפיתוח קבצי צד שרת. פורמט קובץ ZUL פותח על ידי ZK, מסגרת ממשק משתמש המאפשרת לך לבנות אפליקציות אינטרנט ומובייל ללא ידיעת JavaScript או AJAX.

## פורמט קובץ ZUL

קובצי ZUL הם מבוססי XML, המורכבים מאלמנטים שונים לבניית ממשק משתמש. מטעין ZK משתמש בכל רכיב XML כדי ליצור רכיב. העיבוד הכולל של רכיבי העמוד כגון כותרת העמוד, תיאור וכו' מתוארים על ידי כל הוראת עיבוד XML של ZUML.

### ZUL דוגמה

בדוגמה הבאה של קוד ZUML, השורה הראשונה מציינת את כותרת העמוד, השורה השנייה יוצרת רכיב שורש עם כותרת וגבול, והשורה השלישית יוצרת כפתור עם תווית ומאזין אירועים.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
ניתן להוריד את סכימת ZUL מהכתובת http://www.zkoss.org/2005/zul/zul.xsd.
## הפניות

* [ZUL - מאת ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [סכימה ZUL](http://www.zkoss.org/2005/zul/zul.xsd)

