{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "שפה משובצת מאיה", "קובץ", "הרחבה", "פורמט קובץ", "מאיה 3D", "מדריך תכנות" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Maya Embedded File Format",
  "description":"למד על פורמט קובץ MEL וממשקי API שיכולים ליצור ולפתוח קובצי MEL.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## מהו קובץ MEL?

קובץ עם סיומת .mel (Maya Embedded Language) הוא שפת סקריפטים המשמשת את Autodesk Maya ליצירת ממשקים גרפיים. זה מאפשר לך להפוך את היצירה של אלמנטים גרפיים לאוטומטיים באמצעות סקריפטים הניתנים להפעלה בנוסף לממשק הגרפי של מאיה. MEL מאפשרת לך ליצור ממשקים גרפיים מבלי ללמוד תכנות. זה מושג על ידי יצירת מאקרו ופעולות מותאמות אישית שמאיצות משימות שחוזרות על עצמן. נהלים ותסריטים אלה מאפשרים לך ליצור מודלים מותאמים אישית, אנימציות, דינמיקה ועיבוד משימות. ניתן להשתמש ב-Autodesk Maya 2020 כדי לפתוח ולהציג תוכן של קובץ EML.

## פורמט קובץ MEL - מידע נוסף

[מדריך עזר](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) זמין למפתחים במדור התיעוד של מאיה. MEL מבוסס על פקודות סקריפטים של מעטפת, בדומה ל-UINX, כדי להשיג דברים. הפקודות המבוססות על סקריפט הופכות אותו ללא רלוונטי לתכנות קונבנציונלי ומונחה עצמים (OOP), וכתוצאה מכך אין שימוש במבני נתונים, פונקציות קריאה או שימוש ב-OOP כמו בשפות אחרות.

כמה נקודות מפתח לגבי MEL הן כדלקמן.

`הערות` - כל משפט ב-MEL חייב להסתיים בנקודה-פסיק (;), גם בסוף בלוק.

`ערכים חוזרים` - ציון ביטוי שמחזיר ערך אינו מדפיס אוטומטית את הערך ב-MEL. במקום זאת זה גורם לשגיאה.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`פקודות ליצירה, עריכה ומחיקה` - אותה פקודה משמשת ליצירת דברים, עריכת דברים או שאילתת מידע על דברים קיימים. עם זאת, דגל שולט במה (יצירה, עריכה או שאילתה) הפקודה עושה.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`החזר ערך מפונקציה` - תחביר פונקציה מחזיר באופן אוטומטי ערך. כדי לקבל ערך החזרה באמצעות תחביר הפקודה, עליך לצרף את הפקודה במירכאות אחורה.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## הפניות

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

