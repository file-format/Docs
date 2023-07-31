{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml","archivo cshtml", "formato de archivo cshtml", "tipo de archivo cshtml", "archivo", "tipo", "qué es un archivo cshtml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML: página web de ASP.NET Razor",
  "description":"Obtenga información sobre el formato de archivo CSHTML y las API que pueden crear y abrir archivos CSHTML",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## ¿Qué es un archivo CSHTML?

Un archivo con la extensión .cshtml es un archivo HTML [C#](/es/programming/cs/) que el motor Razor Markup utiliza en el lado del servidor para representar los archivos de la página web en el navegador del usuario. Esta codificación del lado del servidor es similar a la página ASP.NET estándar que permite la creación de contenido web dinámico sobre la marcha a medida que la página web se escribe en el navegador. El servidor ejecuta el código del lado del servidor dentro de la página antes de enviar la página generada al navegador. Tareas complejas como acceder a bases de datos y renderizar vistas complejas. Los archivos CSHTML se pueden generar y programar con Microsoft Visual Studio.

## Formato de archivo CSHTML

Los archivos CSHTML son archivos de texto que siguen la sintaxis descrita por el motor de marcado Razor. Razor es compatible con C# y VB.NET, y es más fácil de aprender y usar que ASP y ASP.NET clásicos. w3schools tiene una guía simple pero efectiva para [sintaxis de C# y VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) codificación de Razor.

### Ejemplo CSHTML

El siguiente es un ejemplo de código C# utilizado en un archivo CSHTML para Razor.

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

El código VB.NET equivalente para Razor es el siguiente.

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

## Referencias

* [Referencia de sintaxis de Razor - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

