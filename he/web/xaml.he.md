{
  "date" : "2019-10-11",
  "keywords" :[ "xaml","קובץ xaml", "פורמט קובץ xaml", "סוג קובץ xaml", "קובץ", "סוג", "מהו קובץ xaml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAML - XML Based Markup Language",
  "description":"למד על פורמט קובץ XAML וממשקי API שיכולים ליצור ולפתוח קובצי XAML.",
  "linktitle" : "XAML ",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ XAML?

XAML, Extensible Application Markup Language, קבצי הרחבה מתארים את רכיבי ממשק המשתמש עבור יישומי תוכנה המבוססים על Windows Presentation Foundation (WPF). למרות שפה, אין צורך לתכנת אותה מכיוון שהיא מבוססת על פורמט סטנדרטי של **[XML](/he/web/xml/)** שקל לשימוש והבנה. XAML (מבוטא בשם "zammel") פותח על ידי מיקרוסופט במטרה ספציפית ליצור ממשקי משתמש. ראשי התיבות המקוריים שלו עמדו על Extensible Avalon Markup Language, כאשר Avalon היה שם הקוד של WPF. קבצי XAML נשמרים לפעמים גם עם סיומת XOML.

## יישומי XAML

XAML הוא בחירת השימוש בטכנולוגיות .NET Framework 3.0 ו-.NET Framework 4.0 כגון WPF, Silverlight, Windows Workflow Foundation (WF) ועוד מעטים אחרים. רכיבי ממשק משתמש, כריכות נתונים, אירועים ותכונות אחרות מוגדרים על ידי טפסי XAML ב-WPF. באופן דומה, ניתן להגדיר זרימות עבודה ב-WF באמצעות XAML. זה מעובד בקלות על ידי כלים מהסיבה שהוא מבוסס על XML. מכיוון שזו שפה הצהרתית ואינה זקוקה לקומפילציה, צצים הרבה מוצרים המבוססים על יישומים מבוססי XAML. כל דבר שנוצר או מיושם ב-XAML יכול לבוא לידי ביטוי באמצעות שפת NET מסורתית יותר, כגון C# או Visual Basic .NET.

## פורמט קובץ XAML

XAML מבוסס לחלוטין על פורמט XML. המפרט הראשוני של [מיפוי אובייקטים XAML](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML%5D.pdf) פורסמו ב- 2006, ואחריה [גרסה] נוספת (https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf) שפורסמה ב- 2009. מפרטים אלה מגדירים שני מודלים מופשטים של מידע:

* XAML Schema Information Set Model
* דגם סט מידע XAML

מערך המידע של Xaml (בקיצור 'Xaml Infoset') מגדיר את מבנה המידע שמופע Xaml יכול לייצג. ערכת המידע של סכימת Xaml מאפשרת להגדיר אוצר מילים ספציפי של Xaml. מפרט זה מגדיר גם קבוצה של כללים להפיכת מסמך XML לערכת מידע Xaml. XML הוא פורמט נפוץ עבור Xaml. (המונח "מסמך Xaml" מתייחס למסמך XML המייצג מערך מידע של Xaml.) אך בעוד שמפרט זה אינו מגדיר ייצוגים אחרים, ניתן להשתמש בכל ייצוג פיזי כל עוד הוא יכול לייצג את המידע בערכת המידע של Xaml .

## הפניות

* [XAML - מאת ויקיפדיה](https://en.wikipedia.org/wiki/Extensible_Application_Markup_Language)
* [מפרט פורמט קובץ XAML](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf)

