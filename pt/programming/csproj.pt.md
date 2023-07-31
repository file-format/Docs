{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"Saiba mais sobre o formato de arquivo CSPROJ e APIs que podem criar e abrir arquivos CSPROJ.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## O que é um arquivo CSProj?
Arquivos com extensão CSPROJ representam um arquivo de projeto C# que contém a lista de arquivos incluídos em um projeto junto com as referências aos assemblies do sistema. Quando um novo projeto é iniciado no Microsoft VIiual Studio, você obtém um arquivo .csproj junto com o arquivo de solução principal ([.sln](/pt/programming/sln/)). Se houver mais de um assemblies em um projeto, haverá um número igual de arquivos de projeto também onde o arquivo .sln os une como parte do projeto. O conteúdo desse arquivo define todos os requisitos necessários para construir o projeto, como conteúdo a ser incluído, os requisitos da plataforma, informações de versão, configurações do servidor web ou do servidor de banco de dados e as tarefas que devem ser executadas. O conteúdo de um arquivo de projeto é organizado em formato de arquivo XML e pode ser aberto em qualquer editor de texto para edição e visualização. Ele também fornece uma visão lógica dos arquivos do projeto para um arranjo adequado.

## Formato de arquivo CSPROJ #

Os desenvolvedores podem criar arquivos de projeto por conta própria, respeitando o [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx). A estrutura aberta e transparente dos arquivos de projeto permite que os desenvolvedores de aplicativos imponham um controle sofisticado e refinado sobre como os projetos são criados e implantados. O conteúdo de tal arquivo de projeto tem uma relação muito clara entre si. A figura a seguir mostra os elementos-chave e o relacionamento entre eles para esse arquivo de projeto.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

As seções a seguir elaboram os elementos de formato de arquivo para um arquivo de projeto.

### Elemento do projeto ###

O elemento [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) é o elemento raiz de cada arquivo de projeto. Ele identifica o esquema XML para o arquivo de projeto e pode incluir atributos para especificar os pontos de entrada para o processo de construção.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Propriedades e Condições

As propriedades representam as informações necessárias para construir um projeto. Essas propriedades são definidas em um elemento [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx). Essas propriedades consistem em pares chave-valor em que o nome do elemento da propriedade define a chave da propriedade e o conteúdo do elemento define o valor da propriedade. Por exemplo, você pode definir propriedades denominadas ServerName e ConnectionString para armazenar um nome de servidor estático e uma cadeia de conexão.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

As condições podem ser especificadas por meio de elementos para especificar os critérios de avaliação do elemento. Isso é especificado pela palavra Condição ao definir a propriedade conforme mostrado abaixo:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Quando o MSBuild processa essa definição de propriedade, ele primeiro verifica se um valor de propriedade **$(OutputRoot)** está disponível. Se o valor da propriedade estiver em branco, ou seja, o usuário não forneceu um valor para essa propriedade, a condição será avaliada como **true** e o valor da propriedade será definido como **..\Publish\Out.**

### Itens e Grupos de Itens

Um arquivo de projeto define entradas para o processo de construção que são, na verdade, tipos de arquivos diferentes. Na nomenclatura do MSBuild, essas entradas são representadas por elementos Item e são definidas em um elemento [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx). Assim como os elementos **Propriedade**, você pode nomear um elemento **Item** como quiser. No entanto, você deve especificar um atributo **Include** para identificar o arquivo ou curinga que o item representa.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Metas e Tarefas

Um elemento [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) representa uma instrução de compilação individual (ou tarefa). O MSBuild inclui várias tarefas predefinidas. Por exemplo:

* A tarefa **Copiar** copia os arquivos para um novo local.
* A tarefa **Csc** invoca o compilador Visual C#.
* A tarefa **Vbc** invoca o compilador Visual Basic.
* A tarefa **Exec** executa um programa especificado.
* A tarefa **Message** grava uma mensagem em um registrador.

As tarefas sempre devem estar contidas nos elementos [Destino](https://msdn.microsoft.com/library/t50z2hka.aspx). Um elemento **Target** é um conjunto de uma ou mais tarefas executadas sequencialmente, e um arquivo de projeto pode conter vários destinos.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Referências

* [Compreendendo o arquivo de projeto - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- Arquivo)

