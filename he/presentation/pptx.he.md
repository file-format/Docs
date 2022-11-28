{
  "date" : "2019-12-13",
  "keywords" :[ "קובץ pptx", "פורמט קובץ pptx", "מהו קובץ pptx", "קובץ", "דוגמה לpptx", "סיומת קובץ pptx","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ PPTX וממשקי API שיכולים ליצור ולפתוח קובצי PPTX.",
  "title" :"PPTX - פורמט קובץ מצגת PowerPoint",
  "linktitle" : "PPTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ PPTX?

קבצים עם סיומת PPTX הם קבצי מצגת שנוצרו עם יישום Microsoft PowerPoint הפופולרי. בניגוד לגרסה הקודמת של פורמט קובץ המצגת PPT שהיה בינארי, פורמט PPTX מבוסס על פורמט קובץ מצגת ה-XML הפתוחה של Microsoft PowerPoint. קובץ מצגת הוא אוסף של שקפים שבהם כל שקופית יכולה להכיל טקסט, תמונות, עיצוב, אנימציות ומדיה אחרת. שקופיות אלו מוצגות לקהל בצורה של מצגות עם הגדרות מצגת מותאמות אישית.

## היסטוריה קצרה

פורמט קובץ PPTX הוצג בשנת 2007 ומשתמש בתקן Open XML שהותאם על ידי מיקרוסופט עוד בשנת 2000. לפני PPTX, פורמט הקובץ הנפוץ בו נעשה שימוש היה PPT שהיה פורמט קובץ בינארי טהור. סוג הקובץ החדש הוסיף יתרונות של גדלי קבצים קטנים, פחות שינויים של שחיתות וייצוג תמונות מעוצבות היטב. זה היה בתחילת שנת 2000 כאשר מיקרוסופט החליטה ללכת על השינוי כדי להתאים את התקן עבור **Office Open XML**. עד 2007, פורמט הקובץ החדש הזה הפך לחלק מ-Office 2007 והוא ממשיך גם בגרסאות החדשות של Microsoft Office.

## מפרטי פורמט קובץ PPTX

קבצים שנוצרו בפורמט קובץ Open XML של Office הוא אוסף של קובצי XML יחד עם קבצים אחרים המספקים קישורים בין כל הקבצים המרכיבים אותם. אוסף זה הוא למעשה ארכיון דחוס שניתן לחלץ כדי לראות את תוכנו. כדי לעשות זאת, פשוט שנה את שם סיומת הקובץ PPTX ל-zip וחלץ אותה לצורך התבוננות בתוכן שלה (ראה [מפרט פורמט קובץ PPTX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-pptx/ efd8bb2d-d888-4e2e-af25-cad476730c9f) מאת מיקרוסופט).

הסעיפים הבאים שופכים מעט אור על כל אחד מאלה.

### [Content_Types].xml

זהו הקובץ היחיד שנמצא ברמת הבסיס בעת חילוץ ה-zip. הוא מפרט את סוגי התוכן עבור חלקים בתוך החבילה. כל ההפניות לקובצי ה-XML הכלולים בחבילה מוזכרות בקובץ ה-XML הזה. להלן סוג תוכן עבור חלק שקף:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

אם יש צורך להוסיף חלקים חדשים לחבילה, ניתן לעשות זאת על ידי הוספת החלק החדש ולעדכן את כל הקשרים בתוך קבצי ה-rels. יש לזכור שעבור שינוי כזה, יש לעדכן גם את ה-Content_Types.xml.

### \_rels (תיקיה) ###

היחסים בין החלקים והמשאבים האחרים מחוץ לחבילה נשמרים על ידי חלק היחסים. התיקיה Relationships מכילה קובץ XML יחיד המאחסן את קשרי הגומלין ברמת החבילה. קישורים לחלקי המפתח של קבצי PPTX כלולים בקובץ זה כ-URI. URIs אלה מזהים את סוג הקשר של כל חלק מפתח לחבילה. זה כולל את הקשר למסמך המשרד הראשי הממוקם כ-ppt/presentation.xml וחלקים אחרים בתוך docProps כמאפייני ליבה ומורחבים.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```

לכל חלק במסמך המהווה מקור של קשר אחד או יותר יהיה חלק קשרים משלו כאשר כל חלק של קשר כזה נמצא בתוך תיקיית משנה \_rels של החלק ונקרא על ידי הוספה של '.rels' לשם של המסמך. חֵלֶק. לחלק התוכן הראשי (presentation.xml) יש חלק מערכות יחסים משלו (presentation.xml.rels). הוא מכיל קשרים לחלקים אחרים של התוכן כגון slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, וכן את ה-URI לקישורים חיצוניים.

#### קשר מפורש ####

עבור קשר מפורש, הפניה למשאב מתבצעת באמצעות התכונה Id של a<Relationship> אֵלֵמֶנט. כלומר, ה-ID במקור ממפה ישירות ל-ID של פריט קשר, עם הפניה מפורשת למטרה.

לדוגמה, שקופית עשויה להכיל היפר-קישור כגון זה:

```
<a:hlinkClick r:id#"rId2">
```

ה-r:id#"rId2" מתייחס ליחסים הבאים בתוך חלק הקשרים עבור השקופית (slide1.xml.rels).

```
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
```

#### קשר מרומז ####

עבור מערכת יחסים מרומזת, אין התייחסות ישירה כזו ל-`<Relationship> מזהה`. במקום זאת, ההתייחסות מובנת.

### ppt תיקיית ###

זוהי התיקיה הראשית המכילה את כל הפרטים על תוכן המצגת. כברירת מחדל, יש לו את התיקיות הבאות:

* \_rels
* נושא
* שקופיות
* פריסות שקופיות
* slideMasters

וקבצי ה-XML הבאים:

* presentation.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## הפניות ##

* [[MS-PPTX] - פורמט קובץ PPTX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

