{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"En savoir plus sur le format de fichier CSPROJ et les API qui peuvent créer et ouvrir des fichiers CSPROJ.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Qu'est-ce qu'un fichier CSProj ?
Les fichiers avec l'extension CSPROJ représentent un fichier de projet C# qui contient la liste des fichiers inclus dans un projet ainsi que les références aux assemblys système. Lorsqu'un nouveau projet est lancé dans Microsoft VIiual Studio, vous obtenez un fichier .csproj avec le fichier de solution principal ([.sln](/fr/programming/sln/)). S'il y a plusieurs assemblages dans un projet, il y aura également un nombre égal de fichiers de projet où le fichier .sln les liera tous ensemble dans le cadre du projet. Le contenu de ce fichier définit toutes les exigences requises pour créer le projet, telles que le contenu à inclure, les exigences de la plate-forme, les informations de version, les paramètres du serveur Web ou du serveur de base de données et les tâches à effectuer. Le contenu d'un fichier de projet est organisé au format de fichier XML et peut être ouvert dans n'importe quel éditeur de texte pour modification et visualisation. Il donne également une vue logique aux fichiers de projet pour une disposition appropriée.

## Format de fichier CSPROJ #

Les développeurs peuvent créer eux-mêmes des fichiers de projet et respecter le [schéma XML MSBuild](https://msdn.microsoft.com/library/5dy88c2e.aspx). La structure ouverte et transparente des fichiers de projet permet aux développeurs d'applications d'imposer un contrôle sophistiqué et précis sur la manière dont les projets sont créés et déployés. Le contenu d'un tel fichier de projet a une relation très claire entre eux. La figure suivante montre les éléments clés et la relation entre ceux-ci pour un tel fichier de projet.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

Les sections suivantes détaillent les éléments de format de fichier pour un fichier de projet.

### Élément de projet ###

L'élément [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) est l'élément racine de chaque fichier de projet. Il identifie le schéma XML du fichier de projet et peut inclure des attributs pour spécifier les points d'entrée du processus de génération.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Propriétés et conditions

Les propriétés représentent les informations nécessaires pour construire un projet. Ces propriétés sont définies dans un élément [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx). Ces propriétés se composent de paires clé-valeur où le nom de l'élément de propriété définit la clé de propriété et le contenu de l'élément définit la valeur de la propriété. Par exemple, vous pouvez définir des propriétés nommées ServerName et ConnectionString pour stocker un nom de serveur statique et une chaîne de connexion.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Des conditions peuvent être spécifiées via des éléments afin de spécifier les critères d'évaluation de l'élément. Ceci est spécifié par le mot Condition lors de la définition de la propriété comme indiqué ci-dessous :

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Lorsque MSBuild traite cette définition de propriété, il vérifie d'abord si une valeur de propriété **$(OutputRoot)** est disponible. Si la valeur de la propriété est vide, c'est-à-dire que l'utilisateur n'a pas fourni de valeur pour cette propriété, la condition prend la valeur **true** et la valeur de la propriété est définie sur **..\Publish\Out.**

### Articles et groupes d'articles

Un fichier de projet définit les entrées du processus de construction qui sont en fait des types de fichiers différents. Dans la nomenclature MSBuild, ces entrées sont représentées par des éléments Item et sont définies dans un élément [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx). Tout comme les éléments **Property**, vous pouvez nommer un élément **Item** comme bon vous semble. Cependant, vous devez spécifier un attribut **Inclure** pour identifier le fichier ou le caractère générique que l'élément représente.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Cibles et tâches

Un élément [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) représente une instruction de génération individuelle (ou tâche). MSBuild comprend une multitude de tâches prédéfinies. Par exemple:

* La tâche **Copier** copie les fichiers vers un nouvel emplacement.
* La tâche **Csc** appelle le compilateur Visual C#.
* La tâche **Vbc** appelle le compilateur Visual Basic.
* La tâche **Exec** exécute un programme spécifié.
* La tâche **Message** écrit un message dans un enregistreur.

Les tâches doivent toujours être contenues dans les éléments [Target](https://msdn.microsoft.com/library/t50z2hka.aspx). Un élément **Target** est un ensemble d'une ou plusieurs tâches qui sont exécutées de manière séquentielle, et un fichier de projet peut contenir plusieurs cibles.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Références

* [Comprendre le fichier de projet - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)

