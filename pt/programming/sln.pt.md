{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Saiba mais sobre o formato de arquivo SLN e APIs que podem criar e abrir arquivos SLN.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## O que é arquivo SLN?
Um arquivo com extensão .SLN representa um arquivo de **solução Visual Studio** que mantém informações sobre a organização de projetos em um arquivo de solução. O conteúdo de tal arquivo de solução é escrito em texto simples dentro do arquivo e pode ser observado/editado abrindo o arquivo em qualquer editor de texto. As informações contidas em um arquivo de solução permanecem persistentes e são usadas para carregar as informações associadas à solução, como [projetos](/pt/programming/csproj/) e qualquer outra informação necessária. Os arquivos de projeto referenciados pelo arquivo de solução contêm informações adicionais para permitir que o ambiente preencha a hierarquia com os itens desse projeto. Nenhum dado é armazenado no arquivo .sln, embora as informações do projeto possam ser gravadas no arquivo .sln, se necessário.

## **Histórico de versões do SLN** ##

A versão do formato da solução evoluiu com cada solução do Microsoft Visual Studio com o passar do tempo. Os detalhes sobre estes são os seguintes.


|Versão do Visual Studio|Versão do formato da solução
---|---|
|2003|8,00
|2005|9,00
|2008|10,00
|2010|11,00
|2013|12h00
|2015|12h00
|2017|12h00

### **Conteúdo de um arquivo de solução** ###

Um arquivo de solução consiste em várias seções que são lidas pelo ambiente para carregar o projeto. Um exemplo de conteúdo de arquivo .sln é mostrado abaixo.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **Declaração do Projeto** ###

Um arquivo de solução pode conter mais de uma declaração de projetos e também de diferentes tipos de projeto. Por exemplo, um único arquivo de solução pode conter um projeto CSharp e também um projeto VB.NET. Esses tipos são diferenciados em uma solução usando o [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). A declaração do projeto acima pode ser generalizada como segue para uma compreensão clara.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` O Project-Type-GUID é exclusivo para diferentes tipos de projeto e é usado pelo leitor da solução para identificar o tipo de projeto. Nesse caso, F184B08F-C81C-45F6-A57F-5ABD9991F28F mostra que é um projeto VB.NET.

`GUID do projeto:` O GUID exclusivo do projeto que o diferencia de outros projetos na solução. O ID exclusivo de um projeto na solução possibilita que outros projetos na solução o acessem.

Com base nas informações contidas na seção de projeto do arquivo .sln, o ambiente carrega cada arquivo de projeto. O próprio projeto é então responsável por preencher a hierarquia do projeto e carregar quaisquer projetos aninhados. Quaisquer alterações feitas na solução são salvas de volta no arquivo de solução ao salvar ou fechar o projeto.

## Projeto VS de solução do Visual Studio

**Projeto:** Logicamente, quando você começa a criar um aplicativo ou software usando o Visual Studio, você inicia um novo projeto. Um projeto contém todos os arquivos necessários, como código-fonte, ícones, imagens, arquivos de dados e muito mais, que serão compilados em um aplicativo executável, site ou biblioteca.

**Solução:** uma solução contém um ou mais projetos. Portanto, a solução é como um contêiner para projetos do Visual Studio. Logicamente, podemos dizer que alguém deseja obter uma solução completa para seu negócio, incluindo um site, aplicativo de desktop, serviço tranquilo e aplicativo móvel.

### **Referências** ###

* [Arquivo de solução - por MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [GUIDs de tipo de projeto](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

