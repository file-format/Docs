{
  "date" : "2019-10-11",
  "keywords" :["cshtml","cshtml文件","cshtml文件格式","cshtml文件类型","文件","类型","什么是cshtml文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - ASP.NET Razor 网页",
  "description":"了解 CSHTML 文件格式和可以创建和打开 CSHTML 文件的 API。",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## 什么是 .cshtml 文件？

具有 .cshtml 扩展名的文件是 [C#](/zh/programming/cs/) HTML 文件，Razor 标记引擎在服务器端使用该文件将网页文件呈现给用户的浏览器。此服务器端编码类似于标准 ASP.NET 页面，可在将网页写入浏览器时动态创建 Web 内容。服务器在将生成的页面发送到浏览器之前执行页面内的服务器端代码。访问数据库和渲染复杂视图等复杂任务。 CSHTML 文件可以使用 Microsoft Visual Studio 生成和编程。

## CSHTML 文件格式

CSHTML 文件是遵循 Razor 标记引擎概述的语法的文本文件。 Razor 同时支持 C# 和 VB.NET，比经典的 ASP 和 ASP.NET 易于学习和使用。 w3schools 为 Razor 的 [C# 和 VB.NET 的语法](https://www.w3schools.com/asp/razor_syntax.asp) 编码提供了一个简单而有效的指南。

### CSHTML 示例

以下是 Razor 的 CSHTML 文件中使用的 C# 代码示例。

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

Razor 的等效 VB.NET 代码如下。

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

## 参考

* [Razor 语法参考 - Microsoft](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

