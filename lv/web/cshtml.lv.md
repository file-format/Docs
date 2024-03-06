{
  "date": "2019-10-11",
  "keywords": [
"cshtml",
"cshtml failu",
"cshtml faila formātā",
"cshtml faila tips",
"failu",
"veids",
"kas ir cshtml fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSHTML — vietne ASP.NET Razor",
  "description": "Uzziniet par CSHTML faila formātu un API, kas var izveidot un atvērt CSHTML failus.",
  "linktitle": "CSHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cshtm-lvl"
}
},
  "lastmod": "2021-04-29"
}

## Kas ir CSHTML fails?

Fails ar paplašinājumu .cshtml ir [C#](/programming/cs/) HTML fails, ko servera pusē izmanto Razor Markup programma, lai tīmekļa lapas failus renderētu lietotāja pārlūkprogrammā. Šis servera puses kodējums ir līdzīgs standarta ASP.NET lapai, kas nodrošina dinamisku tīmekļa satura izveidi lidojumā, kad tīmekļa lapa tiek ierakstīta pārlūkprogrammā. Pirms ģenerētās lapas nosūtīšanas uz pārlūkprogrammu serveris lapas iekšpusē izpilda servera puses kodu. Sarežģīti uzdevumi, piemēram, piekļuve datu bāzēm un sarežģītu skatu renderēšana. CSHTML failus var ģenerēt un ieprogrammēt, izmantojot Microsoft Visual Studio.

## CSHTML faila formāts

CSHTML faili ir teksta faili, kas atbilst Razor iezīmēšanas programmas norādītajai sintaksei. Razor atbalsta gan C#, gan VB.NET, un to ir viegli iemācīties un lietot nekā klasisko ASP un ASP.NET. Vietnē w3schools ir vienkāršs, taču efektīvs ceļvedis Razor [syntax of C# and VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) kodēšanai.

### CSHTML piemērs

Tālāk ir sniegts C# koda piemērs, kas tiek izmantots CSHTML failā Razor.

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

Līdzvērtīgs VB.NET kods Razor ir šāds.

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

## Atsauces

* [Razor sintakses atsauce — Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)


