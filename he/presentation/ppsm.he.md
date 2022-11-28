{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ ppsm", "פורמט קובץ ppsm", "מהו קובץ ppsm", "קובץ", "דוגמה לppsm", "סיומת קובץ ppsm","סיומת", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM - קובץ מצגת PowerPoint מאופשר מאקרו",
  "description":"למד על פורמט קובץ PPSM וממשקי API שיכולים ליצור ולפתוח קבצי PPSM.",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ PPSM?

קבצים עם סיומת PPSM מייצגים פורמט קובץ מצגת שקופיות המותאם למאקרו שנוצר עם Microsoft PowerPoint 2007 ומעלה. פורמט קובץ דומה נוסף הוא [PPTM](/he/presentation/pptm/) אשר שונה בפתיחה עם Microsoft PowerPoint בפורמט הניתן לעריכה במקום לרוץ כמצגת שקופיות. בעת הפעלה כמצגת שקופיות, קובץ ה-PPSM מציג את שקופיות המצגת עם תוכן שלם במצגת השקופיות והוא נמצא במצב קריאה בלבד כברירת מחדל. עדיין ניתן לערוך קבצי PPSM ב-Microsoft PowerPoint על-ידי פתיחתם ב-PowerPoint.

## פורמט קובץ ##

פורמט קובץ PPSM הוצג עם PowerPoint 2007 והוא מבוסס על פורמט הקובץ OpenXML המשתמש בשילוב של XML ו-[ZIP](/he/compression/zip/) כדי לאחסן את התוכן שלו. קבצים שנוצרו בפורמט קובץ Open XML של Office הוא אוסף של קובצי XML יחד עם קבצים אחרים המספקים קישורים בין כל הקבצים המרכיבים אותם. אוסף זה הוא למעשה ארכיון דחוס שניתן לחלץ כדי לראות את תוכנו. כדי לעשות זאת, פשוט שנה את שם סיומת הקובץ PPSM עם zip וחלץ אותה כדי לצפות בתוכן שלה.

הסעיפים הבאים שופכים מעט אור על כל אחד מאלה.

### [Content_Types].xml ###

זהו הקובץ היחיד שנמצא ברמת הבסיס בעת חילוץ ה-zip. הוא מפרט את סוגי התוכן עבור חלקים בתוך החבילה. כל ההפניות לקובצי ה-XML הכלולים בחבילה מוזכרות בקובץ ה-XML הזה. להלן סוג תוכן עבור חלק שקף:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
אם יש צורך להוסיף חלקים חדשים לחבילה, ניתן לעשות זאת על ידי הוספת החלק החדש ולעדכן את כל הקשרים בתוך קבצי ה-rels. יש לזכור שעבור שינוי כזה, יש לעדכן גם את ה-Content_Types.xml.

### \_rels (תיקיה) ###

היחסים בין החלקים והמשאבים האחרים מחוץ לחבילה נשמרים על ידי חלק היחסים. התיקיה Relationships מכילה קובץ XML יחיד המאחסן את קשרי הגומלין ברמת החבילה. קישורים לחלקי המפתח של קבצי המצגת כלולים בקובץ זה כ-URI. URIs אלה מזהים את סוג הקשר של כל חלק מפתח לחבילה. זה כולל את הקשר למסמך המשרד הראשי הממוקם כ-ppt/presentation.xml וחלקים אחרים בתוך docProps כמאפייני ליבה ומורחבים.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
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
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
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

* [פורמט קובץ מצגת OpenXML](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

