{
"date": "2023-05-15",
  "keywords": [
"קובץ csx",
"מהו קובץ csx",
"מה מכיל קובץ csx",
"מהו הפורמט של קובץ csx",
"קוֹבֶץ",
"סיומת קובץ csx",
"סיומת"
],
  "author": {
"display_name": "שייק פאיז"
},
"draft": "false",
"toc": true,
"title": "פורמט קובץ CSX - Visual C# Script",
  "description":"למד על פורמט CSX וממשקי API שיכולים ליצור ולפתוח קובצי CSX.",
"linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
      "parent": "programming"
}
},
"lastmod": "2023-05-15"
}

## מהו קובץ CSX?

Visual C# Script (הידוע גם בשם CSX) הוא פורמט קובץ המשמש את מנוע הסקריפטים של Roslyn במערכת האקולוגית .NET של מיקרוסופט. קבצי CSX מכילים קוד C# שניתן להפעיל ישירות ללא צורך בשלב הידור נפרד.

פורמט CSX הוא ספציפי למערכת האקולוגית של מיקרוסופט ולא פורמט קובץ בשימוש נרחב בתכנות כללי. קבצי CSX משמשים לעתים קרובות בתרחישים שבהם נדרשת פונקציונליות של אבות טיפוס או סקריפטים מהירים. הם מאפשרים לך ליצור ולהפעיל תוכניות C# בצורה קלה יותר בהשוואה ליצירת יישום הידור מלא.

כדי להפעיל קבצי CSX, אתה יכול להשתמש בכלים כמו .NET Interactive Notebooks, המספקים סביבה אינטראקטיבית להפעלת קוד C#. Visual Studio Code עם סיומת C# ו-.NET Core SDK יכול לשמש גם לעבודה עם קבצי CSX.

## מה מכיל קובץ CSX?

קובץ CSX (C# Script) מכיל קוד C# שניתן להפעיל ישירות. זה יכול לכלול כל קוד C# חוקי כגון הצהרות משתנים, פונקציות, מחלקות ומבנה תכנות אחר.

הנה דוגמה למה שקובץ CSX עשוי להכיל:

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

קובצי CSX יכולים לכלול גם הצהרות ייבוא, הפניות לספריה חיצוניות ותכונות אחרות של שפת C# כדי לתמוך בפונקציונליות של הקוד. הקוד מתפרש ומבוצע תוך כדי תנועה ללא צורך בהידור מה שהופך אותו למתאים למשימות סקריפטים ואב-טיפוס מהירים.

## מהו הפורמט של קובץ CSX?

פורמט CSX (C# Script) עוקב אחר פורמט מבוסס טקסט פשוט. בדרך כלל יש לו סיומת קובץ .csx כדי להבדיל אותו מקובצי קוד מקור רגילים של C# (.cs).

ניתן לערוך קבצי CSX באמצעות כל עורך טקסט או סביבת פיתוח משולבת (IDE) התומכת בהדגשת תחביר C#. ברגע שקובץ CSX מוכן, ניתן להפעיל אותו באמצעות כלים כמו .NET Interactive Notebooks, ממשק שורת הפקודה .NET Core (CLI), או IDE עם תמיכה בסקריפט C#.

## הפניות
* [תכנות C# עם Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)

