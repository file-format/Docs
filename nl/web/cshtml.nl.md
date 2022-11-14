{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml","cshtml-bestand", "cshtml-bestandsformaat", "cshtml-bestandstype", "bestand", "type", "wat is een cshtml-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - ASP.NET Razor-webpagina",
  "description":"Meer informatie over CSHTML-bestandsindeling en API's die CSHTML-bestanden kunnen maken en openen.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Wat is een CSHTML-bestand?

Een bestand met de extensie .cshtml is een [C#](/nl/programming/cs/) HTML-bestand dat door de Razor Markup-engine aan de serverzijde wordt gebruikt om de webpaginabestanden naar de browser van de gebruiker weer te geven. Deze codering aan de serverzijde is vergelijkbaar met de standaard ASP.NET-pagina, waardoor dynamische webcontent kan worden gemaakt terwijl de webpagina naar de browser wordt geschreven. De server voert de servercode binnen de pagina uit voordat de gegenereerde pagina naar de browser wordt verzonden. Complexe taken zoals toegang tot databases en het weergeven van complexe weergaven. CSHTML-bestanden kunnen worden gegenereerd en geprogrammeerd met Microsoft Visual Studio.

## CSHTML-bestandsindeling

CSHTML-bestanden zijn tekstbestanden die de syntaxis volgen die is beschreven door de Razor-markup-engine. Razor ondersteunt zowel C# als VB.NET, en het is gemakkelijk te leren en te gebruiken dan klassieke ASP en ASP.NET. De w3schools heeft een eenvoudige maar effectieve gids voor [syntaxis van C# en VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) codering van Razor.

### CSHTML-voorbeeld

Hieronder volgt een voorbeeld van een C#-code die wordt gebruikt in een CSHTML-bestand voor Razor.

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

De equivalente VB.NET-code voor Razor is als volgt.

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

## Referenties

* [Razor-syntaxisreferentie - Microsoft](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

