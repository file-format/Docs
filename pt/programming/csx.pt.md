{
"data": "15/05/2023",
  "keywords": [
"arquivo csx",
"o que é um arquivo csx",
"o que contém o arquivo csx",
"qual é o formato do arquivo csx",
"arquivo",
"extensão de arquivo csx",
"extensão"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de arquivo CSX - Script Visual C#",
  "description":"Aprenda sobre o formato CSX e APIs que podem criar e abrir arquivos CSX.",
"linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
"parent" : "programming"
}
},
"último mod": "15/05/2023"
}

## O que é um arquivo .CSX?

Visual C# Script (também conhecido como CSX) é um formato de arquivo usado pelo mecanismo de script Roslyn no ecossistema .NET da Microsoft. Os arquivos CSX contêm código C# que pode ser executado diretamente sem a necessidade de uma etapa de compilação separada.

O formato CSX é específico do ecossistema Microsoft e não é um formato de arquivo amplamente utilizado na programação geral. Os arquivos CSX são frequentemente usados em cenários onde é necessária prototipagem rápida ou funcionalidade de script. Eles permitem que você crie e execute programas C# de maneira mais leve em comparação com a criação de um aplicativo compilado completo.

Para executar arquivos CSX, você pode usar ferramentas como .NET Interactive Notebooks, que fornecem um ambiente interativo para executar código C#. O Visual Studio Code com a extensão C# e o SDK do .NET Core também podem ser usados para trabalhar com arquivos CSX.

## O que o arquivo CSX contém?

Um arquivo CSX (C# Script) contém código C# que pode ser executado diretamente. Pode incluir qualquer código C# válido, como declarações de variáveis, funções, classes e outras construções de programação.

Aqui está um exemplo do que o arquivo CSX pode conter:

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

Os arquivos CSX também podem incluir instruções de importação, referências de bibliotecas externas e outros recursos da linguagem C# para oferecer suporte à funcionalidade do código. O código é interpretado e executado dinamicamente, sem necessidade de compilação, tornando-o adequado para tarefas de script e prototipagem rápida.

## Qual é o formato do arquivo CSX?

O formato CSX (C# Script) segue um formato simples baseado em texto. Normalmente possui a extensão de arquivo .csx para diferenciá-lo dos arquivos de código-fonte C# regulares (.cs).

Os arquivos CSX podem ser editados usando qualquer editor de texto ou ambiente de desenvolvimento integrado (IDE) que suporte realce de sintaxe C#. Quando o arquivo CSX estiver pronto, ele poderá ser executado usando ferramentas como .NET Interactive Notebooks, a interface de linha de comando (CLI) do .NET Core ou um IDE com suporte a scripts C#.

## Referências
* [Programação C# com Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)

