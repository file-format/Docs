{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml","cshtml-Datei", "cshtml-Dateiformat", "cshtml-Dateityp", "Datei", "Typ", "was ist eine cshtml-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - ASP.NET Razor-Webseite",
  "description":"Erfahren Sie mehr über das CSHTML-Dateiformat und APIs, die CSHTML-Dateien erstellen und öffnen können.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Was ist eine CSHTML-Datei?

Eine Datei mit der Erweiterung .cshtml ist eine [C#](/de/programming/cs/)-HTML-Datei, die serverseitig von der Razor Markup-Engine verwendet wird, um die Webseitendateien im Browser des Benutzers zu rendern. Diese serverseitige Codierung ähnelt der standardmäßigen ASP.NET-Seite, die eine dynamische Erstellung von Webinhalten im Handumdrehen ermöglicht, während die Webseite in den Browser geschrieben wird. Der Server führt den serverseitigen Code innerhalb der Seite aus, bevor er die generierte Seite an den Browser sendet. Komplexe Aufgaben wie der Zugriff auf Datenbanken und das Rendern komplexer Ansichten. CSHTML-Dateien können mit Microsoft Visual Studio generiert und programmiert werden.

## CSHTML-Dateiformat

CSHTML-Dateien sind Textdateien, die der von der Razor-Markup-Engine beschriebenen Syntax folgen. Razor unterstützt sowohl C# als auch VB.NET und ist einfacher zu erlernen und zu verwenden als klassisches ASP und ASP.NET. Die w3schools haben eine einfache, aber effektive Anleitung für die [Syntax von C# und VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) Codierung von Razor.

### CSHTML-Beispiel

Es folgt ein C#-Codebeispiel, das in einer CSHTML-Datei für Razor verwendet wird.

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

Der entsprechende VB.NET-Code für Razor lautet wie folgt.

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

## Verweise

* [Razor-Syntaxreferenz – Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

