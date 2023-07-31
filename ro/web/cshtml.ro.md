{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml", "fișier cshtml", "format fișier cshtml", "tip fișier cshtml", "fișier", "tip", "ce este un fișier cshtml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - Pagina web ASP.NET Razor",
  "description":"Aflați despre formatul de fișier CSHTML și despre API-urile care pot crea și deschide fișiere CSHTML.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Ce este un fișier CSHTML?

Un fișier cu extensia .cshtml este un fișier HTML [C#](/ro/programming/cs/) care este utilizat pe partea serverului de către motorul Razor Markup pentru a reda fișierele paginii web în browserul utilizatorului. Această codificare pe partea serverului este similară cu pagina standard ASP.NET, care permite crearea dinamică a conținutului web din mers pe măsură ce pagina web este scrisă în browser. Serverul execută codul de pe partea serverului în interiorul paginii înainte de a trimite pagina generată către browser. Sarcini complexe, cum ar fi accesarea bazelor de date și redarea vizualizărilor complexe. Fișierele CSHTML pot fi generate și programate folosind Microsoft Visual Studio.

## Format de fișier CSHTML

Fișierele CSHTML sunt fișiere text care urmează sintaxa descrisă de motorul de marcare Razor. Razor acceptă atât C#, cât și VB.NET și este ușor de învățat și utilizat decât ASP și ASP.NET clasic. W3schools are un ghid simplu, dar eficient pentru [sintaxa C# și VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) codarea Razor.

### Exemplu CSHTML

Mai jos este un exemplu de cod C# utilizat într-un fișier CSHTML pentru Razor.

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

Codul echivalent VB.NET pentru Razor este următorul.

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

## Referințe

* [Referință de sintaxă Razor - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

