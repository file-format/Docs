{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "קובץ", "סיומת", "פורמט קובץ", "קובץ VB Project", "מדריך תכנות" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"למד על פורמט קובץ VBPROJ וממשקי API שיכולים ליצור ולפתוח קבצי VBPROJ.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## מהו קובץ VBPROJ?

קובץ עם סיומת .vbproj הוא קובץ פרויקט של Microsoft Visual Basic המשמש את מנוע MSBuild של מיקרוסופט לבניית הפרויקטים בתוך פתרון Visual Studio. זה דומה לקובץ [CSPROJ](/he/programming/csproj/) עבור פרויקטי NET שנכתבו ב-[C#](/he/programming/cs/). מנוע MSBuild קורא מידע הכלול בקבוצות שונות מקבצי VBPROJ ומייצר את קובץ הפלט. קובץ VBPROJ יכול להכיל מידע הקשור למזהים גלובליים, מחלקות ומאפיינים המגדירים את הפרויקט. ניתן לפתוח ולערוך קבצי VBPROJ באמצעות Microsoft Visual Studio וכל עורך טקסט נפוץ כגון Notepad במערכות ההפעלה Windows ו-MacOS.

## פורמט קובץ VBPROJ - מידע נוסף

קבצי VBPROJ הם קבצי טקסט שנכתבים בפורמט קובץ [XML](/he/web/xml/) המבוסס על [סכמת XML של MSBuild](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild- project-file-schema-reference?view=vs-2019). קובץ VBPROJ מכיל מידע בצורה של תגי XML המגדירים מידע הקשור לאותה קבוצת הגדרות מסוימת. מומלץ מאוד לפתוח ולערוך את קבצי ההגדרות הללו ב-Microsoft Visual Studio IDE.

### אלמנטים של VBPROJ

המרכיבים המרכיבים של קובץ הגדרות VB הם כפי שמוצג בתמונה הבאה.

{{< figure src="../vbproj.png" alt="פורמט קובץ VBPROJ" >}}

הטבלה הבאה נותנת תיאור קצר של אלמנטים אלה.

|אלמנט|תיאור|
---|---|
|פרויקט| רכיב שורש של כל קובץ פרויקט ויכול לכלול תכונות לציון נקודות הכניסה לתהליך הבנייה בנוסף לזיהוי סכימת XML עבור קובץ הפרויקט|
|מאפיינים ותנאים| מאפיינים מורכבים מזוגות מפתח-ערך ומוגדרים בתוך אלמנט PropertyGroup. שם רכיב המאפיין מייצג את מפתח המאפיין והתוכן של האלמנט מגדיר את ערך המאפיין.|
|Items and ItemGroups|פריטים בקובץ פרויקט הם קלט לתהליך הבנייה כגון קבצי קוד קבצים, קבצי תצורה, קבצי פקודות ואחרים הנדרשים כחלק מתהליך הבנייה. פריטים הם וחייבים להיות מוגדרים בתוך רכיב ItemGroup.|
|יעדים ומשימות| רכיב משימה מייצג הוראת בנייה (או משימה) בודדת. MSBuild כולל מספר רב של משימות מוגדרות מראש כגון Copy, CSC, VBC, Exec. משימות חייבות להיות מוכלות תמיד ב-'Target' Element שהוא קבוצה של משימות אחת או יותר שמבוצעות ברצף, וקובץ פרויקט יכול להכיל מספר יעדים.|

## הפניות

* [הבנת קובץ הפרויקט](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [MSBuild Schema Elements](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

