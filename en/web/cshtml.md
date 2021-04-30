{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CSHTML - ASP.NET Razor Webpage",
  "description":"Learn about CSHTML file format and APIs that can create and open CSHTML files.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-04-29"
}

## What is a CSHTML file?

A file with .cshtml extension is a [C#](/programming/cs/) HTML file that is used at server side by Razor Markup engine to render the webpage files to user's browser. This server side coding is similar to the standard ASP.NET page enabling dynamic web content creation on the fly as the webpage is written to the browser. The server executes the server-side code inside the page before sending the generated page to the browser. Complex tasks such as accessing databases and rendering complex views. CSHTML files can be generated and programmed using Microsoft Visual Studio.

## CSHTML File Format

CSHTML files are text files that follow the syntax outlined by Razor markup engine. Razor supports both C# and VB.NET, and it is easy to learn and use than classic ASP and ASP.NET. The w3schools has a simple yet effective guide for [syntax of C# and VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) coding of Razor.

### CSHTML Example

Following is C# Code example used in a CSHTML file for Razor.

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

The equivalent VB.NET code for Razor is as follow.

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
## How to open CSHTML file?

As mentioned earlier, CSHTML are text files that can be opened in any text editor. Microsoft Visual Studio provides users with suitable programming environment with syntax highlighting and Intellisense while coding CSHTML files.

## References
* [Razor Syntax Reference - Microsoft](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)
* [CSHTML - By w3schools](https://www.w3schools.com/asp/razor_syntax.asp)
