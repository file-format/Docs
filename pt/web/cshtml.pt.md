{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml", "arquivo cshtml", "formato de arquivo cshtml", "tipo de arquivo cshtml", "arquivo", "tipo", "o que é um arquivo cshtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - página da Web ASP.NET Razor",
  "description":"Saiba mais sobre o formato de arquivo CSHTML e APIs que podem criar e abrir arquivos CSHTML.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## O que é um arquivo CSHTML?

Um arquivo com extensão .cshtml é um arquivo HTML [C#](/pt/programming/cs/) usado no lado do servidor pelo mecanismo Razor Markup para renderizar os arquivos da página da Web para o navegador do usuário. Essa codificação do lado do servidor é semelhante à página ASP.NET padrão, permitindo a criação dinâmica de conteúdo da Web em tempo real à medida que a página da Web é gravada no navegador. O servidor executa o código do lado do servidor dentro da página antes de enviar a página gerada para o navegador. Tarefas complexas, como acessar bancos de dados e renderizar visualizações complexas. Os arquivos CSHTML podem ser gerados e programados usando o Microsoft Visual Studio.

## Formato de arquivo CSHTML

Os arquivos CSHTML são arquivos de texto que seguem a sintaxe descrita pelo mecanismo de marcação Razor. Razor oferece suporte a C# e VB.NET, e é fácil de aprender e usar do que ASP e ASP.NET clássicos. O w3schools tem um guia simples mas eficaz para [sintaxe de C# e VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) codificação do Razor.

### Exemplo de CSHTML

A seguir está um exemplo de código C# usado em um arquivo CSHTML para Razor.

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

O código VB.NET equivalente para Razor é o seguinte.

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

## Referências

* [Referência de sintaxe do Razor - Microsoft](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

