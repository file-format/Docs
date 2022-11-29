{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml","cshtml-fil", "cshtml-filformat", "cshtml-filtyp", "fil", "typ", "vad är en cshtml-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - ASP.NET Razor Webpage",
  "description":"Läs mer om CSHTML-filformat och API:er som kan skapa och öppna CSHTML-filer.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Vad är en CSHTML-fil?

En fil med tillägget .cshtml är en [C#](/sv/programming/cs/) HTML-fil som används på serversidan av Razor Markup-motorn för att rendera webbsidesfilerna till användarens webbläsare. Denna kodning på serversidan liknar den vanliga ASP.NET-sidan som möjliggör dynamiskt webbinnehåll när webbsidan skrivs till webbläsaren. Servern kör koden på serversidan på sidan innan den skickar den genererade sidan till webbläsaren. Komplexa uppgifter som att komma åt databaser och rendera komplexa vyer. CSHTML-filer kan genereras och programmeras med hjälp av Microsoft Visual Studio.

## CSHTML filformat

CSHTML-filer är textfiler som följer syntaxen som beskrivs av Razor-markeringsmotorn. Razor stöder både C# och VB.NET, och det är lätt att lära sig och använda än klassiska ASP och ASP.NET. W3schools har en enkel men effektiv guide för [syntax av C# och VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) kodning av Razor.

### CSHTML Exempel

Följande är C#-kodexempel som används i en CSHTML-fil för Razor.

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

Motsvarande VB.NET-kod för Razor är följande.

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

## Referenser

* [Razor Syntax Reference - Microsoft](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

