{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml","file cshtml", "formato file cshtml", "tipo di file cshtml", "file", "tipo", "che cos'è un file cshtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - Pagina Web Razor ASP.NET",
  "description":"Scopri il formato di file CSHTML e le API che possono creare e aprire file CSHTML.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Che cos'è un file CSHTML?

Un file con estensione .cshtml è un file HTML [C#](/it/programming/cs/) utilizzato sul lato server dal motore Razor Markup per eseguire il rendering dei file della pagina Web nel browser dell'utente. Questa codifica lato server è simile alla pagina ASP.NET standard che consente la creazione di contenuti Web dinamici al volo mentre la pagina Web viene scritta nel browser. Il server esegue il codice lato server all'interno della pagina prima di inviare la pagina generata al browser. Attività complesse come l'accesso ai database e il rendering di viste complesse. I file CSHTML possono essere generati e programmati utilizzando Microsoft Visual Studio.

## Formato file CSHTML

I file CSHTML sono file di testo che seguono la sintassi delineata dal motore di markup Razor. Razor supporta sia C# che VB.NET ed è facile da imparare e da usare rispetto ai classici ASP e ASP.NET. Il w3schools ha una guida semplice ma efficace per la codifica [sintassi di C# e VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) di Razor.

### Esempio CSHTML

Di seguito è riportato un esempio di codice C# utilizzato in un file CSHTML per Razor.

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

Il codice VB.NET equivalente per Razor è il seguente.

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

## Riferimenti

* [Riferimento alla sintassi di Razor - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

