{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"למד על פורמט קובץ CSPROJ וממשקי API שיכולים ליצור ולפתוח קובצי CSPROJ.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## מהו קובץ CSProj?
קבצים עם סיומת CSPROJ מייצגים קובץ פרויקט C# המכיל את רשימת הקבצים הכלולים בפרויקט יחד עם ההפניות למכלולי מערכת. כאשר פרויקט חדש מופעל ב-Microsoft VIiual Studio, אתה מקבל קובץ .csproj אחד יחד עם קובץ הפתרון הראשי ([.sln](/he/programming/sln/)). אם יש יותר ממכלול אחד בפרויקט, יהיה מספר שווה של קבצי פרוייקט גם כאשר קובץ ה-.sln קושר את כולם יחד כחלק מהפרויקט. התוכן של קובץ זה מגדיר את כל הדרישות הנדרשות לבניית הפרויקט כגון תוכן שיכלול, דרישות הפלטפורמה, מידע ניהול גרסאות, הגדרות שרת אינטרנט או שרת מסד נתונים, והמשימות שיש לבצע. התוכן של קובץ פרוייקט מסודר בפורמט קובץ XML וניתן לפתוח אותו בכל עורך טקסט לעריכה וגם לצפייה. זה גם נותן תצוגה הגיונית לקבצי הפרויקט לסידור נכון.

## פורמט קובץ CSPROJ #

מפתחים יכולים ליצור קבצי פרויקט בעצמם, כמו גם לכבד את [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx). המבנה הפתוח והשקוף של קבצי הפרויקט מאפשר למפתחי יישומים להטיל שליטה מתוחכמת ועדינה על אופן הבנייה והפריסה של הפרויקטים. לתוכן של קובץ פרויקט כזה יש קשר מאוד ברור בינם לבין עצמם. האיור הבא מציג אלמנטים מרכזיים והקשר ביניהם עבור קובץ פרויקט כזה.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

הסעיפים הבאים מרחיבים את רכיבי פורמט הקובץ עבור קובץ פרוייקט.

### אלמנט פרויקט ###

האלמנט [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) הוא אלמנט הבסיס של כל קובץ פרויקט. הוא מזהה את סכימת ה-XML עבור קובץ הפרויקט ויכול לכלול תכונות לציון נקודות הכניסה לתהליך הבנייה.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### מאפיינים ותנאים

נכסים מייצגים את המידע הדרוש לבניית פרויקט. מאפיינים כאלה מוגדרים בתוך אלמנט [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx). מאפיינים אלה מורכבים מזוגות מפתח-ערך כאשר שם רכיב המאפיין מגדיר את מפתח המאפיין והתוכן של האלמנט מגדיר את ערך המאפיין. לדוגמה, תוכל להגדיר מאפיינים בשם ServerName ו- ConnectionString כדי לאחסן שם שרת סטטי ומחרוזת חיבור.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

ניתן לציין תנאים באמצעות אלמנטים על מנת לציין את הקריטריונים להערכת האלמנט. זה מצוין על ידי מילת תנאי בזמן הגדרת המאפיין כפי שמוצג להלן:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

כאשר MSBuild מעבד את הגדרת המאפיין הזה, הוא בודק תחילה אם ערך מאפיין **$(OutputRoot)** זמין. אם ערך המאפיין ריק - במילים אחרות, המשתמש לא סיפק ערך עבור מאפיין זה - התנאי מוערך ל-**true** וערך המאפיין מוגדר ל-**..\Publish\Out.**

### פריטים וקבוצות פריטים

קובץ פרויקט מגדיר תשומות לתהליך הבנייה שהם למעשה סוגי קבצים שונים. במינוח MSBuild, כניסות אלה מיוצגות על ידי רכיבי פריט ומוגדרות בתוך אלמנט [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx). בדיוק כמו אלמנטים של **נכס**, אתה יכול לתת שם לרכיב **פריט** איך שתרצה. עם זאת, עליך לציין מאפיין **Include** כדי לזהות את הקובץ או התו הכללי שהפריט מייצג.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### יעדים ומשימות

אלמנט [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) מייצג הוראת בנייה (או משימה) בודדת. MSBuild כולל מספר רב של משימות מוגדרות מראש. לדוגמה:

* המשימה **העתק** מעתיקה קבצים למיקום חדש.
* המשימה **Csc** מפעילה את מהדר Visual C#.
* המשימה **Vbc** מפעילה את מהדר Visual Basic.
* המשימה **Exec** מריצה תוכנית מוגדרת.
* המשימה **הודעה** כותבת הודעה ל-logger.

משימות חייבות תמיד להיות כלולות בתוך רכיבי [Target](https://msdn.microsoft.com/library/t50z2hka.aspx). אלמנט **יעד** הוא קבוצה של משימות אחת או יותר המבוצעות ברצף, וקובץ פרויקט יכול להכיל מספר יעדים.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## הפניות

* [הבנת קובץ הפרויקט - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)

