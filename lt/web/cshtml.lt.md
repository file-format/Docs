{
  "date": "2019-10-11",
  "keywords": [
"cshtml",
"cshtml failą",
"cshtml failo formatas",
"cshtml failo tipas",
"failą",
"tipo",
"kas yra cshtml failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSHTML – ASP.NET Razor tinklalapis",
  "description": "Sužinokite apie CSHTML failo formatą ir API, kurios gali kurti ir atidaryti CSHTML failus.",
  "linktitle": "CSHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cshtm-ltl"
}
},
  "lastmod": "2021-04-29"
}

## Kas yra CSHTML failas?

Failas su plėtiniu .cshtml yra [C#](/programming/cs/) HTML failas, kurį serveryje naudoja Razor Markup variklis, kad tinklalapio failai būtų pateikiami vartotojo naršyklėje. Šis serverio pusės kodavimas yra panašus į standartinį ASP.NET puslapį, leidžiantį greitai kurti dinaminį žiniatinklio turinį, kai tinklalapis įrašomas į naršyklę. Prieš išsiųsdamas sugeneruotą puslapį į naršyklę, serveris puslapio viduje vykdo serverio kodą. Sudėtingos užduotys, pvz., prieiga prie duomenų bazių ir sudėtingų vaizdų atvaizdavimas. CSHTML failus galima generuoti ir programuoti naudojant Microsoft Visual Studio.

## CSHTML failo formatas

CSHTML failai yra tekstiniai failai, atitinkantys Razor žymėjimo variklio apibrėžtą sintaksę. Razor palaiko ir C#, ir VB.NET, jį lengva išmokti ir naudoti nei klasikinį ASP ir ASP.NET. W3schools turi paprastą, bet veiksmingą Razor kodavimo [syntax of C# and VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) vadovą.

### CSHTML pavyzdys

Toliau pateikiamas C# kodo pavyzdys, naudojamas Razor CSHTML faile.

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

Lygiavertis Razor VB.NET kodas yra toks.

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

## Nuorodos

* [Skustuvo sintaksės nuoroda – „Microsoft“](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)


