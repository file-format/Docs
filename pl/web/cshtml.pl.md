{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml","plik cshtml", "format pliku cshtml", "typ pliku cshtml", "plik", "typ", "co to jest plik cshtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML — strona internetowa ASP.NET Razor",
  "description":"Poznaj format plików CSHTML i interfejsy API, które mogą tworzyć i otwierać pliki CSHTML.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Co to jest plik CSHTML?

Plik z rozszerzeniem .cshtml to plik HTML [C#](/pl/programming/cs/), który jest używany po stronie serwera przez aparat Razor Markup do renderowania plików strony internetowej w przeglądarce użytkownika. To kodowanie po stronie serwera jest podobne do standardowej strony ASP.NET, umożliwiając dynamiczne tworzenie treści internetowych w locie, gdy strona jest zapisywana w przeglądarce. Serwer wykonuje kod po stronie serwera wewnątrz strony przed wysłaniem wygenerowanej strony do przeglądarki. Złożone zadania, takie jak uzyskiwanie dostępu do baz danych i renderowanie złożonych widoków. Pliki CSHTML można generować i programować za pomocą Microsoft Visual Studio.

## Format pliku CSHTML

Pliki CSHTML to pliki tekstowe zgodne ze składnią opisaną przez silnik znaczników Razor. Razor obsługuje zarówno C#, jak i VB.NET, i jest łatwy do nauczenia się i używania niż klasyczne ASP i ASP.NET. W3schools ma prosty, ale skuteczny przewodnik po [składni C# i VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) kodowania Razor.

### Przykład CSHTML

Poniżej znajduje się przykład kodu C# używany w pliku CSHTML dla Razor.

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

Odpowiednik kodu VB.NET dla Razor jest następujący.

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

## Bibliografia

* [Informacje o składni Razor — Microsoft](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

