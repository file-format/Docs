{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml", "soubor cshtml", "formát souboru cshtml", "typ souboru cshtml", "soubor", "typ", "co je soubor cshtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - Webová stránka ASP.NET Razor",
  "description":"Další informace o formátu souboru CSHTML a rozhraních API, která mohou vytvářet a otevírat soubory CSHTML.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Co je soubor CSHTML?

Soubor s příponou .cshtml je soubor HTML [C#](/cs/programming/cs/), který na straně serveru používá stroj Razor Markup k vykreslení souborů webové stránky do prohlížeče uživatele. Toto kódování na straně serveru je podobné standardní stránce ASP.NET umožňující vytváření dynamického webového obsahu za běhu, když je webová stránka zapsána do prohlížeče. Server spustí kód na straně serveru uvnitř stránky před odesláním vygenerované stránky do prohlížeče. Komplexní úlohy, jako je přístup k databázím a vykreslování komplexních pohledů. Soubory CSHTML lze generovat a programovat pomocí Microsoft Visual Studio.

## Formát souboru CSHTML

Soubory CSHTML jsou textové soubory, které se řídí syntaxí navrženou značkovacím strojem Razor. Razor podporuje C# i VB.NET a je snadné se ho naučit a používat než klasické ASP a ASP.NET. W3schools má jednoduchý, ale účinný průvodce pro [syntaxi C# a VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) kódování Razor.

### Příklad CSHTML

Následuje příklad kódu C# použitý v souboru CSHTML pro Razor.

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

Ekvivalentní kód VB.NET pro Razor je následující.

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

## Reference

* [Reference syntaxe Razor – Microsoft](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

