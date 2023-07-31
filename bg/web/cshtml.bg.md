{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml", "cshtml файл", "cshtml файлов формат", "cshtml тип файл", "файл", "тип", "какво е cshtml файл" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML – ASP.NET Razor уеб страница",
  "description":"Научете за CSHTML файловия формат и API, които могат да създават и отварят CSHTML файлове.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Какво е CSHTML файл?

Файл с разширение .cshtml е [C#](/bg/programming/cs/) HTML файл, който се използва от страната на сървъра от Razor Markup engine за изобразяване на файловете на уеб страниците в браузъра на потребителя. Това кодиране от страна на сървъра е подобно на стандартната ASP.NET страница, което позволява динамично създаване на уеб съдържание в движение, докато уеб страницата се записва в браузъра. Сървърът изпълнява кода от страната на сървъра вътре в страницата, преди да изпрати генерираната страница към браузъра. Сложни задачи като достъп до бази данни и изобразяване на сложни изгледи. CSHTML файловете могат да бъдат генерирани и програмирани с помощта на Microsoft Visual Studio.

## CSHTML файлов формат

CSHTML файловете са текстови файлове, които следват синтаксиса, очертан от машината за маркиране на Razor. Razor поддържа C# и VB.NET и е лесен за научаване и използване от класическите ASP и ASP.NET. W3schools има просто, но ефективно ръководство за [синтаксис на C# и VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) кодиране на Razor.

### Пример за CSHTML

Следва пример за C# код, използван в CSHTML файл за Razor.

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

Еквивалентният VB.NET код за Razor е както следва.

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

## Препратки

* [Справка за синтаксис на Razor - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

