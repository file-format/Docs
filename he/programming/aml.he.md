
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ AML - Microsoft Assistance Markup Language File",
  "description":"למד על מהו קובץ AML וממשקי API שיכולים ליצור ולפתוח קובצי AML.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML - Microsoft Assistance Markup Language File

## מהו קובץ AML?

קובץ AML (Assistance Markup Language) הוא קובץ XML שנוצר עם Microsoft Assistance Markup Language (MAML). זה פותח על ידי Microsoft כדי לספק עזרה מקוונת עבור מערכת ההפעלה של Microsoft Windows. לפני כן, העזרה של Windows הייתה זמינה בפורמט הקובץ HTML [CHM](/he/web/chm/). קובצי AML מספקים מסמך מובנה המאפשר ליישום ליצור קוד מקור ודפי עזרה תומכים. זה מאפשר הגדרה של מסמכים והמרכיבים המרכיבים אותם לפי ההקשר שלהם. קובצי העזרה של AML מתפרסמים באופן מקוון וניתן להגדיר אותם כך שיעודכנו מתוך עדכוני החבילות הזמינים באינטרנט.

## מבנה קובץ MAML

קובצי AML שנוצרים באמצעות MAML נשמרים כקבצי [XML](/he/web/xml/) שניתן להשתמש בהם כדי לבטא מגוון רחב של מושגים פעילים. זה יכול גם לספק עזרה מודרכת (אשף תוכן פעיל) שהופך את קובץ העזרה לאינטראקטיבי עבור המשתמש עם אשף שלב אחר שלב.

קובץ AML שנוצר באמצעות MAML עוקב אחר מבנה הכתיבה שלו שניתן לחלק למקטעים כמו:

* קונספטואלי
* שאלות נפוצות
* מילון מונחים
* תהליך
* התייחסות
* תוכן לשימוש חוזר
* משימה
* פתרון בעיות, ו
* הדרכה

## כיצד ליצור קבצי MAML?

ניתן ליצור קובצי MAML באחת מהשיטות הבאות:

* שימוש ב-Sandcastle - משתמש בחבילה של סכימות וקובצי הפעלה של תוכניות ליצירת קובץ העזרה. עם זאת, כלי זה הופסק.
* שימוש ב-DocProject - תוסף Microsoft Visual Studio שניתן להפעיל מתוך Microsoft Visual Studio להפקת תוכן העזרה.

ניתן ליצור קובצי MAML באמצעות Sandcastle, חבילה של סכימות XSL וקובצי הפעלה של תוכניות. הם עשויים גם להיווצר באמצעות DocProject, תוסף כלי כתיבה לעזרה של Microsoft Visual Studio.

## הפניות

* [צור עזרה מבוססת XML באמצעות PlatyPS
](https://docs.microsoft.com/en-us/powershell/scripting/dev-cross-plat/create-help-using-platyps?view=powershell-7.2)
* [Microsoft Assistance Markup Language](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML - Arc Macro Language File

## מהו קובץ ARC Macro AML?

קובץ AML (ARC Macro Language) הוא קובץ סקריפטים שנוצר עם יישום ArcInfo Workstation GIS. הוא כתוב בשפת המאקרו ARC, שהיא שפה אלגוריתמית קניינית ברמה גבוהה ליצירת יישומי GIS ב-ArcInfo. AML תוכנן על ידי ESRI בשנת 1986 ושירת את המטרה של יצירת יישומים ממערכת שורת הפקודה שלהם ARCINFO GIS. בהיותם קובץ סקריפט, קבצי AML יכולים להכיל פקודות סקריפט לביצוע מספר משימות כגון יצירת רכיבי ממשק משתמש ותפעול נתוני מפה.

## פורמט קובץ AML - מידע נוסף

AML, בהיותו קבצי סקריפטים, שמור את המידע בדיסק כקובצי טקסט רגיל. הוא עוקב אחר תחביר AML שהתבסס על שפת המעטפת של CPL של מערכת ההפעלה PRIMOS. שפת AML הוחלפה על ידי מסגרת העיבוד הגיאוגרפי של ESRI שהיא חלק מחבילת ArcGIS ומשתמשת ב-ArcObjects כדי לספק תמיכה בתכנות באמצעות VBA או Python.

## הפניות

* [שפת מאקרו של ARC](https://en.wikipedia.org/wiki/ARC_Macro_Language)
* [שימוש ב-AML עם כלי סקריפט](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

