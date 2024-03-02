{
  "date": "2019-10-11",
  "keywords": [
"cshtml",
"comhad cshtml",
"Formáid comhaid cshtml",
"Cineál comhaid cshtml",
"comhad",
"cineál",
"Cad é an comhad cshtml"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSHTML - Leathanach Gréasáin Razor ASP.NET",
  "description": "Foghlaim faoi fhormáid comhaid CSHTML agus APIanna ar féidir leo comhaid CSHTML a chruthú agus a oscailt.",
  "linktitle": "CSHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cshtm-gal"
}
},
  "lastmod": "2021-04-29"
}

## Cad is comhad CSHTML ann?

Is comhad HTML {{ HYPERLINK1}} é comhad a bhfuil iarmhír .cshtml air a úsáideann inneall Razor Markup ar thaobh an fhreastalaí chun comhaid an leathanaigh ghréasáin a sholáthar do bhrabhsálaí an úsáideora. Tá an códú taobh freastalaí seo cosúil leis an leathanach caighdeánach ASP.NET a chumasaíonn cruthú ábhar gréasáin dinimiciúil ar an eitilt de réir mar a scríobhtar an leathanach gréasáin chuig an mbrabhsálaí. Déanann an freastalaí an cód freastalaí taobh istigh den leathanach a fhorghníomhú roimh an leathanach ginte a sheoladh chuig an mbrabhsálaí. Tascanna casta ar nós rochtain a fháil ar bhunachair shonraí agus tuairimí casta a thabhairt. Is féidir comhaid CSHTML a ghiniúint agus a ríomhchlárú trí úsáid a bhaint as Microsoft Visual Studio.

## Formáid Chomhaid CSHTML

Comhaid téacs is ea comhaid CSHTML a leanann an chomhréir atá leagtha amach ag inneall marcála Razor. Tacaíonn Razor le C# agus VB.NET araon, agus is fusa é a fhoghlaim agus a úsáid ná asp clasaiceach agus ASP.NET. Tá treoir shimplí ach éifeachtach ag na w3schools maidir le [syntax of C# and VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) códú Razor.

### Sampla CSHTML

Seo a leanas sampla Cód C# a úsáidtear i gcomhad CSHTML le haghaidh Razor.

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

Seo a leanas an cód VB.NET comhionann le haghaidh Razor.

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

## Tagairtí

* [Tagairt Comhréire Razor - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)


