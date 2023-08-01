{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "arquivo", "extensão", "formato de arquivo", "Arquivo de projeto VB", "Guia de programação" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"Saiba mais sobre o formato de arquivo VBPROJ e APIs que podem criar e abrir arquivos VBPROJ.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## O que é um arquivo VBPROJ?

Um arquivo com extensão .vbproj é um arquivo de projeto do Microsoft Visual Basic que é usado pelo mecanismo MSBuild da Microsoft para criar os projetos em uma solução do Visual Studio. É semelhante ao arquivo [CSPROJ](/pt/programming/csproj/) para projetos .NET escritos em [C#](/pt/programming/cs/). O mecanismo MSBuild lê as informações contidas em diferentes grupos dos arquivos VBPROJ e gera o arquivo de saída. Um arquivo VBPROJ pode conter informações relacionadas a identificadores globais, classes e propriedades que definem o projeto. Os arquivos VBPROJ podem ser abertos e editados usando o Microsoft Visual Studio e qualquer editor de texto comum, como o Bloco de Notas nos sistemas operacionais Windows e MacOS.

## Formato de arquivo VBPROJ - Mais informações

Os arquivos VBPROJ são arquivos textuais escritos no formato de arquivo [XML](/pt/web/xml/) com base no [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019). Um arquivo VBPROJ contém informações na forma de tags XML que definem informações relacionadas a esse grupo específico de configurações. É altamente recomendável abrir e editar esses arquivos de configuração no Microsoft Visual Studio IDE.

### Elementos VBPROJ

Os elementos constituintes de um arquivo de configurações do VB são mostrados na imagem a seguir.

{{< figure src="../vbproj.png" alt="Formato de arquivo VBPROJ" >}}

A tabela a seguir fornece uma breve descrição desses elementos.

|Elemento|Descrição|
---|---|
|Projeto| Elemento raiz de cada arquivo de projeto e pode incluir atributos para especificar os pontos de entrada para o processo de construção, além de identificar o esquema XML para o arquivo de projeto|
|Propriedades e Condições| As propriedades consistem em pares chave-valor e são definidas dentro de um elemento PropertyGroup. O nome do elemento de propriedade representa a chave de propriedade e o conteúdo do elemento define o valor da propriedade.|
|Items e ItemGroups|Items em um arquivo de projeto são entradas para o processo de construção, como arquivos de código de arquivos, arquivos de configuração, arquivos de comando e outros necessários como parte do processo de construção. Os itens são e devem ser definidos em um elemento ItemGroup.|
|Destinos e Tarefas| Um elemento Task representa uma instrução de construção individual (ou tarefa). O MSBuild inclui várias tarefas predefinidas, como Copiar, CSC, VBC, Exec. As tarefas devem estar sempre contidas em um elemento `Target` que é um conjunto de uma ou mais tarefas que são executadas sequencialmente, e um arquivo de projeto pode conter vários destinos.|

## Referências

* [Compreendendo o arquivo do projeto](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [Elementos de esquema do MSBuild](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

