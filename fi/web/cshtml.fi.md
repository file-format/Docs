{
  "date": "2019-10-11",
  "keywords": [
"cshtml",
"cshtml tiedosto",
"cshtml-tiedostomuoto",
"cshtml-tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on cshtml-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSHTML - ASP.NET Razor -verkkosivu",
  "description": "Opi CSHTML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CSHTML-tiedostoja.",
  "linktitle": "CSHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cshtm-fil"
}
},
  "lastmod": "2021-04-29"
}

## Mikä on CSHTML-tiedosto?

Tiedosto, jonka laajennus on .cshtml, on [C#](/programming/cs/) HTML-tiedosto, jota Razor Markup -moottori käyttää palvelimen puolella verkkosivun tiedostojen näyttämiseen käyttäjän selaimeen. Tämä palvelinpuolen koodaus on samanlainen kuin tavallinen ASP.NET-sivu, joka mahdollistaa dynaamisen verkkosisällön luomisen lennossa, kun verkkosivu kirjoitetaan selaimeen. Palvelin suorittaa palvelinpuolen koodin sivulla ennen luodun sivun lähettämistä selaimeen. Monimutkaiset tehtävät, kuten tietokantojen käyttö ja monimutkaisten näkymien luominen. CSHTML-tiedostoja voidaan luoda ja ohjelmoida Microsoft Visual Studiolla.

## CSHTML-tiedostomuoto

CSHTML-tiedostot ovat tekstitiedostoja, jotka noudattavat Razor-merkintämoottorin määrittelemää syntaksia. Razor tukee sekä C# että VB.NET, ja se on helppo oppia ja käyttää kuin klassiset ASP ja ASP.NET. w3schoolsilla on yksinkertainen mutta tehokas opas Razorin [syntax of C# and VB.NET](https://www.w3schools.com/asp/razor_syntax.asp)-koodaukseen.

### CSHTML-esimerkki

Seuraavassa on esimerkki C#-koodista, jota käytetään Razorin CSHTML-tiedostossa.

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

Vastaava VB.NET-koodi Razorille on seuraava.

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

## Viitteet

* [Razorin syntaksiviittaus – Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)


