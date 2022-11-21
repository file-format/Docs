{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "arquivo", "extensão", "formato de arquivo", "CSharp", "Linguagem de Programação" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - Arquivo de código CSharp",
  "description":"Saiba mais sobre o formato de arquivo CS e APIs que podem criar e abrir arquivos CS.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo CS?

Arquivos com extensão .cs são arquivos de código-fonte para a linguagem de programação C#. Introduzido pela Microsoft para uso com o .NET Framework, o formato de arquivo fornece a linguagem de programação de baixo nível para escrever código compilado para gerar o arquivo de saída final na forma de EXE ou DLL. Eles podem ser criados e compilados com o Microsoft Visual Studio. O Microsoft Visual Studio Express também pode ser usado para criar e atualizar esses arquivos, que é um IDE gratuito. Os arquivos CS são usados para o desenvolvimento de aplicativos que podem variar de aplicativos de desktop simples a programas mais complexos. Um projeto simples do Visual Studio [solução](/pt/programming/sln/) criado com a linguagem C# pode incluir um ou mais desses arquivos. Os arquivos marcados para inclusão na compilação são listados no arquivo [CSPROJ](/pt/programming/csproj/) que faz parte do projeto e informa ao compilador para usar os arquivos marcados.

## Formato de arquivo CS ##

Os arquivos CS são formatos de arquivo baseados em texto que podem ser abertos em qualquer editor de texto para edição. No entanto, quando aberto em um IDE compatível com realce de sintaxe adequado, o código é fácil de ler e organizar. Um arquivo CS simples contém:

* Declaração de namespaces - Para se referir a uma funcionalidade específica definida por esse namespace específico
* Declaração de variáveis - Para declarar variáveis de nível de classe para a implementação específica
* Declaração de métodos - Para declarar a declaração de métodos para a funcionalidade específica

### Sintaxe ###

* O ponto e vírgula é usado para indicar o final de uma instrução.
* As chaves são usadas para agrupar declarações. As instruções são comumente agrupadas em métodos (funções), métodos em classes e classes em namespaces.
* As variáveis são atribuídas usando um sinal de igual, mas comparadas usando dois sinais de igual consecutivos.
* Colchetes são usados com arrays, tanto para declará-los quanto para obter um valor em um determinado índice em um deles.

### Exemplo ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

