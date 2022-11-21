{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "arquivo", "extensão", "formato de arquivo", "Visual Basic", "Guia de programação" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Arquivo de código do Visual Basic",
  "description":"Saiba mais sobre o formato de arquivo VB e APIs que podem criar e abrir arquivos VB.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo VB?

Um arquivo VB é um arquivo de código-fonte criado na linguagem Visual Basic que foi criado pela Microsoft para desenvolvimento de aplicativos .NET. Outra linguagem semelhante com sintaxe diferente é C# cujos arquivos são salvos com extensão de arquivo [.CS](/pt/programming/cs/). O formato de arquivo fornece a linguagem de programação de baixo nível para escrever código que é compilado para gerar o arquivo de saída final na forma de EXE ou DLL. Eles podem ser criados e compilados com o Microsoft Visual Studio. O Microsoft Visual Studio Express também pode ser usado para criar e atualizar esses arquivos, que é um IDE gratuito. Um projeto simples do Visual Studio [solução](/pt/programming/sln/) criado com a linguagem VB pode incluir um ou mais desses arquivos. Os arquivos marcados para inclusão na compilação são listados no arquivo [CSPROJ](/pt/programming/csproj/) que faz parte do projeto e informa ao compilador para usar os arquivos marcados.

## Formato de arquivo VB - Mais informações

Os arquivos VB são formatos de arquivo baseados em texto que podem ser abertos em qualquer editor de texto para edição. No entanto, quando aberto em um IDE compatível com realce de sintaxe adequado, o código é fácil de ler e organizar. Um arquivo VB simples contém:

* Declaração de namespaces - Para se referir a uma funcionalidade específica definida por esse namespace específico
* Declaração de variáveis - Para declarar variáveis de nível de classe para a implementação específica
* Declaração de métodos - Para declarar a declaração de métodos para a funcionalidade específica

## Exemplo de formato de arquivo VB

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



