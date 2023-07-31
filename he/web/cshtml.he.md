{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml","cshtml file", "cshtml file format", "cshtml file type", "file", "type", "what is a cshtml file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - ASP.NET Razor Webpage",
  "description":"למד על פורמט קובץ CSHTML וממשקי API שיכולים ליצור ולפתוח קובצי CSHTML.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## מהו קובץ CSHTML?

קובץ עם סיומת .cshtml הוא קובץ HTML [C#](/he/programming/cs/) המשמש בצד השרת על ידי מנוע ה-Razor Markup כדי להציג את קבצי דפי האינטרנט לדפדפן המשתמש. קידוד זה בצד השרת דומה לעמוד הסטנדרטי של ASP.NET המאפשר יצירת תוכן אינטרנט דינמי תוך כדי כתיבת דף האינטרנט לדפדפן. השרת מבצע את הקוד בצד השרת בתוך הדף לפני שליחת הדף שנוצר לדפדפן. משימות מורכבות כגון גישה למאגרי מידע ועיבוד תצוגות מורכבות. ניתן ליצור ולתכנת קובצי CSHTML באמצעות Microsoft Visual Studio.

## פורמט קובץ CSHTML

קובצי CSHTML הם קבצי טקסט העוקבים אחר התחביר המתואר על ידי מנוע הסימון של Razor. Razor תומך גם ב-C# וגם ב-VB.NET, וקל ללמוד ולהשתמש בה מאשר ASP ו-ASP.NET הקלאסיות. ל-w3schools יש מדריך פשוט אך יעיל לקידוד [תחביר של C# ו-VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) של Razor.

### דוגמה לCSHTML

להלן דוגמה לקוד C# המשמש בקובץ CSHTML עבור Razor.

```
<!-- Single statement block -->
@{ var myMessage = "Hello World"; }

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@{
var greeting = "Welcome to our site!";
var weekDay = DateTime.Now.DayOfWeek;
var greetingMessage = greeting + " Here in Huston it is: " + weekDay;
}
<p>The greeting is: @greetingMessage</p>
```

קוד VB.NET המקביל עבור Razor הוא כדלקמן.

```
<!-- Single statement block  -->
@Code dim myMessage = "Hello World" End Code

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@Code
dim greeting = "Welcome to our site!"
dim weekDay = DateTime.Now.DayOfWeek
dim greetingMessage = greeting & " Here in Huston it is: " & weekDay
End Code

<p>The greeting is: @greetingMessage</p>
```

## הפניות

* [הפניה לתחביר תער - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

