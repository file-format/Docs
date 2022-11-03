{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml", "файл cshtml", "формат файла cshtml", "тип файла cshtml", "файл", "тип", "что такое файл cshtml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML — веб-страница ASP.NET Razor",
  "description":"Узнайте о формате файла CSHTML и API-интерфейсах, которые могут создавать и открывать файлы CSHTML.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## .CSHTML вариант №

Файл с расширением .cshtml представляет собой HTML-файл [C#](/ru/programming/cs/), который используется на стороне сервера механизмом разметки Razor для отображения файлов веб-страницы в браузере пользователя. Это кодирование на стороне сервера похоже на стандартную страницу ASP.NET, позволяющую создавать динамическое веб-содержимое «на лету», когда веб-страница записывается в браузер. Сервер выполняет серверный код внутри страницы перед отправкой сгенерированной страницы в браузер. Сложные задачи, такие как доступ к базам данных и рендеринг сложных представлений. Файлы CSHTML можно создавать и программировать с помощью Microsoft Visual Studio.

## Формат файла CSHTML

Файлы CSHTML — это текстовые файлы, которые следуют синтаксису, описанному механизмом разметки Razor. Razor поддерживает как C#, так и VB.NET, и его легче изучить и использовать, чем классический ASP и ASP.NET. В w3schools есть простое, но эффективное руководство по [синтаксису C# и VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) кодированию Razor.

### Пример CSHTML

Ниже приведен пример кода C#, используемый в файле CSHTML для Razor.

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

Эквивалентный код VB.NET для Razor выглядит следующим образом.

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

## использованная литература

* [Справочник по синтаксису Razor — Microsoft] (https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

