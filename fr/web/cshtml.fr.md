{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml","fichier cshtml", "format de fichier cshtml", "type de fichier cshtml", "fichier", "type", "qu'est-ce qu'un fichier cshtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - Page Web ASP.NET Razor",
  "description":"En savoir plus sur le format de fichier CSHTML et les API qui peuvent créer et ouvrir des fichiers CSHTML.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Qu'est-ce qu'un fichier CSHTML ?

Un fichier avec l'extension .cshtml est un fichier HTML [C#](/fr/programming/cs/) qui est utilisé côté serveur par le moteur Razor Markup pour restituer les fichiers de la page Web au navigateur de l'utilisateur. Ce codage côté serveur est similaire à la page ASP.NET standard permettant la création de contenu Web dynamique à la volée lorsque la page Web est écrite dans le navigateur. Le serveur exécute le code côté serveur à l'intérieur de la page avant d'envoyer la page générée au navigateur. Tâches complexes telles que l'accès aux bases de données et le rendu de vues complexes. Les fichiers CSHTML peuvent être générés et programmés à l'aide de Microsoft Visual Studio.

## Format de fichier CSHTML

Les fichiers CSHTML sont des fichiers texte qui suivent la syntaxe décrite par le moteur de balisage Razor. Razor prend en charge à la fois C # et VB.NET, et il est facile à apprendre et à utiliser que les ASP et ASP.NET classiques. w3schools propose un guide simple mais efficace pour le codage [syntaxe de C# et VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) de Razor.

### Exemple CSHTML

Voici un exemple de code C# utilisé dans un fichier CSHTML pour Razor.

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

Le code VB.NET équivalent pour Razor est le suivant.

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

## Références

* [Référence de la syntaxe Razor - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

