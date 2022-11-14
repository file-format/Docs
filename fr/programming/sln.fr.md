{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"En savoir plus sur le format de fichier SLN et les API qui peuvent créer et ouvrir des fichiers SLN.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier SLN ?
Un fichier avec l'extension .SLN représente un fichier **Solution Visual Studio** qui conserve des informations sur l'organisation des projets dans un fichier de solution. Le contenu d'un tel fichier de solution est écrit en texte brut à l'intérieur du fichier et peut être observé/modifié en ouvrant le fichier dans n'importe quel éditeur de texte. Les informations contenues dans un fichier de solution restent persistantes et sont utilisées pour charger les informations associées à la solution telles que [projets](/fr/programmation/csproj/) et toute autre information requise. Les fichiers de projet référencés par le fichier de solution contiennent des informations supplémentaires permettant à l'environnement de remplir la hiérarchie avec les éléments de ce projet. Aucune donnée n'est stockée dans le fichier .sln, bien que les informations du projet puissent être écrites dans le fichier .sln si nécessaire.

## **Historique des versions SLN** ##

La version du format de la solution a évolué avec chaque solution Microsoft Visual Studio au fil du temps. Les détails à ce sujet sont les suivants.


|Version Visual Studio|Version du format de la solution
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Contenu d'un fichier de solution** ###

Un fichier de solution se compose de plusieurs sections qui sont lues par l'environnement pour charger le projet. Un exemple de contenu de fichier .sln est illustré ci-dessous.

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

### **Déclaration de projet** ###

Un fichier de solution peut contenir plus d'une déclaration de projets et cela aussi de différents types de projets. Par exemple, un seul fichier de solution peut contenir un CSharp ainsi qu'un projet VB.NET. Ces types sont distingués dans une solution utilisant le [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). La déclaration de projet ci-dessus peut être généralisée comme suit pour une compréhension claire.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID :` Le Project-Type-GUID est unique pour différents types de projets et est utilisé par le lecteur de solution pour identifier le type de projet. Dans ce cas, F184B08F-C81C-45F6-A57F-5ABD9991F28F indique qu'il s'agit d'un projet VB.NET.

`Project GUID:` Le GUID unique du projet qui le différencie des autres projets de la solution. L'ID unique d'un projet dans la solution permet aux autres projets de la solution d'y accéder.

En fonction des informations contenues dans la section projet du fichier .sln, l'environnement charge chaque fichier projet. Le projet lui-même est alors chargé de remplir la hiérarchie du projet et de charger tous les projets imbriqués. Toutes les modifications apportées à la solution sont enregistrées dans le fichier de solution lors de l'enregistrement ou de la fermeture du projet.

## Solution Visual Studio VS projet

**Projet :** Logiquement, lorsque vous commencez à créer une application ou un logiciel à l'aide de Visual Studio, vous démarrez un nouveau projet. Un projet contient tous les fichiers nécessaires tels que le code source, les icônes, les images, les fichiers de données, etc., qui seront compilés dans une application exécutable, un site Web ou une bibliothèque.

**Solution :** Une solution contient un ou plusieurs projets. La solution est donc comme un conteneur pour les projets Visual Studio. Logiquement, nous pouvons dire que quelqu'un souhaite obtenir une solution complète pour son entreprise, y compris un site Web, une application de bureau, un service reposant et une application mobile.

### **Références** ###

* [Fichier de solution - Par MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [GUID de type de projet] (https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

