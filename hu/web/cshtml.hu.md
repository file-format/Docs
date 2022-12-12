{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml", "cshtml fájl", "cshtml fájlformátum", "cshtml fájltípus", "fájl", "típus", "mi az a cshtml fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML – ASP.NET Razor Weboldal",
  "description":"További információ a CSHTML fájlformátumról és az API-król, amelyek CSHTML-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Mi az a CSHTML fájl?

A .cshtml kiterjesztésű fájl egy [C#](/hu/programming/cs/) HTML-fájl, amelyet a Razor Markup motor a szerver oldalon használ a weboldal fájlok megjelenítésére a felhasználó böngészőjében. Ez a szerveroldali kódolás hasonló a szabványos ASP.NET-oldalhoz, amely lehetővé teszi a dinamikus webtartalom-létrehozást, miközben a weboldalt a böngészőbe írják. A szerver végrehajtja a szerveroldali kódot az oldalon belül, mielőtt elküldi a generált oldalt a böngészőnek. Összetett feladatok, például adatbázisok elérése és összetett nézetek megjelenítése. A CSHTML fájlok a Microsoft Visual Studio segítségével hozhatók létre és programozhatók.

## CSHTML fájlformátum

A CSHTML fájlok olyan szöveges fájlok, amelyek a Razor jelölőmotor által felvázolt szintaxist követik. A Razor támogatja a C#-ot és a VB.NET-et is, és könnyen megtanulható és használható, mint a klasszikus ASP és ASP.NET. A w3schools egy egyszerű, de hatékony útmutatóval rendelkezik a Razor [C# és VB.NET szintaxisa](https://www.w3schools.com/asp/razor_syntax.asp) kódolásához.

### CSHTML példa

A következő példa a Razor CSHTML-fájljában használt C# kódra.

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

A Razor megfelelő VB.NET kódja a következő.

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

## Hivatkozások

* [Razor Syntax Reference – Microsoft](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

