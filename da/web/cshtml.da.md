{
  "date": "2019-10-11",
  "keywords": [
"cshtml",
"cshtml fil",
"cshtml filformat",
"cshtml filtype",
"fil",
"type",
"hvad er en cshtml-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSHTML - ASP.NET Razor webside",
  "description": "Lær om CSHTML-filformat og API'er, der kan oprette og åbne CSHTML-filer.",
  "linktitle": "CSHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cshtm-dal"
}
},
  "lastmod": "2021-04-29"
}

## Hvad er en CSHTML fil?

En fil med filtypen .cshtml er en [C#](/programming/cs/) HTML-fil, der bruges på serversiden af Razor Markup-motoren til at gengive websidefilerne til brugerens browser. Denne serversidekodning svarer til standard ASP.NET-siden, der muliggør dynamisk webindholdsskabelse på farten, mens websiden skrives til browseren. Serveren udfører server-side-koden inde på siden, før den sender den genererede side til browseren. Komplekse opgaver såsom adgang til databaser og gengivelse af komplekse visninger. CSHTML-filer kan genereres og programmeres ved hjælp af Microsoft Visual Studio.

## CSHTML filformat

CSHTML filer er tekstfiler, der følger syntaksen skitseret af Razor markup engine. Razor understøtter både C# og VB.NET, og det er nemt at lære og bruge end klassiske ASP og ASP.NET. w3schools har en enkel, men effektiv guide til [syntax of C# and VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) kodning af Razor.

### CSHTML Eksempel

Følgende er C#-kodeeksempel brugt i en CSHTML-fil til Razor.

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

Den tilsvarende VB.NET-kode til Razor er som følger.

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

## Referencer

* [Razor Syntax Reference - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)


