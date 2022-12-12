{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml", "файл cshtml", "формат файлу cshtml", "тип файлу cshtml", "файл", "тип", "що таке файл cshtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - веб-сторінка ASP.NET Razor",
  "description":"Дізнайтеся про формат файлу CSHTML та API, які можуть створювати та відкривати файли CSHTML.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Що таке файл CSHTML?

Файл із розширенням .cshtml — це [C#](/uk/programming/cs/) HTML-файл, який використовується на стороні сервера механізмом розмітки Razor для відтворення файлів веб-сторінок у браузері користувача. Це кодування на стороні сервера схоже на стандартну сторінку ASP.NET, що дозволяє створювати динамічний веб-вміст на льоту, коли веб-сторінка записується в браузер. Сервер виконує серверний код усередині сторінки перед тим, як відправити згенеровану сторінку в браузер. Складні завдання, такі як доступ до баз даних і візуалізація складних представлень. Файли CSHTML можна створювати та програмувати за допомогою Microsoft Visual Studio.

## Формат файлу CSHTML

Файли CSHTML — це текстові файли, які відповідають синтаксису, визначеному механізмом розмітки Razor. Razor підтримує як C#, так і VB.NET, його легше освоїти та використовувати, ніж класичні ASP та ASP.NET. У w3schools є простий, але ефективний посібник із [синтаксису C# і VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) кодування Razor.

### Приклад CSHTML

Нижче наведено приклад коду C#, який використовується у файлі CSHTML для Razor.

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

Еквівалентний код VB.NET для Razor такий.

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

## Список літератури

* [Довідник із синтаксису Razor – Microsoft](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

