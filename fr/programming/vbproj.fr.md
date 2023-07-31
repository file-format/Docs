{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "fichier", "extension", "format de fichier", "Fichier de projet VB", "Guide de programmation" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"En savoir plus sur le format de fichier VBPROJ et les API qui peuvent créer et ouvrir des fichiers VBPROJ.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Qu'est-ce qu'un fichier VBPROJ ?

Un fichier avec l'extension .vbproj est un fichier de projet Microsoft Visual Basic utilisé par le moteur MSBuild de Microsoft pour générer les projets dans une solution Visual Studio. Il est similaire au fichier [CSPROJ](/fr/programming/csproj/) pour les projets .NET écrits en [C#](/fr/programming/cs/). Le moteur MSBuild lit les informations contenues dans différents groupes à partir des fichiers VBPROJ et génère le fichier de sortie. Un fichier VBPROJ peut contenir des informations relatives aux identificateurs globaux, aux classes et aux propriétés qui définissent le projet. Les fichiers VBPROJ peuvent être ouverts et modifiés à l'aide de Microsoft Visual Studio et de tout éditeur de texte courant tel que le Bloc-notes sur les systèmes d'exploitation Windows et MacOS.

## Format de fichier VBPROJ - Plus d'informations

Les fichiers VBPROJ sont des fichiers texte écrits au format de fichier [XML](/fr/web/xml/) basé sur le [schéma XML MSBuild](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild- project-file-schema-reference?view=vs-2019). Un fichier VBPROJ contient des informations sous la forme de balises XML qui définissent les informations relatives à ce groupe particulier de paramètres. Il est fortement recommandé d'ouvrir et de modifier ces fichiers de paramètres dans Microsoft Visual Studio IDE.

### Éléments VBPROJ

Les éléments constitutifs d'un fichier de paramètres VB sont illustrés dans l'image suivante.

{{< figure src="../vbproj.png" alt="Format de fichier VBPROJ" >}}

Le tableau suivant donne une brève description de ces éléments.

|Élément|Description|
---|---|
|Projet| Élément racine de chaque fichier de projet et peut inclure des attributs pour spécifier les points d'entrée du processus de construction en plus d'identifier le schéma XML pour le fichier de projet|
|Propriétés et Conditions| Les propriétés sont constituées de paires clé-valeur et sont définies dans un élément PropertyGroup. Le nom de l'élément de propriété représente la clé de propriété et le contenu de l'élément définit la valeur de la propriété.|
|Items and ItemGroups|Les éléments d'un fichier de projet sont des entrées du processus de génération, telles que des fichiers de code de fichiers, des fichiers de configuration, des fichiers de commande et d'autres éléments requis dans le cadre du processus de génération. Les éléments sont et doivent être définis dans un élément ItemGroup.|
|Cibles et tâches| Un élément Task représente une instruction de construction individuelle (ou tâche). MSBuild comprend une multitude de tâches prédéfinies telles que Copy, CSC, VBC, Exec. Les tâches doivent toujours être contenues dans un élément `Target` qui est un ensemble d'une ou plusieurs tâches exécutées séquentiellement, et un fichier projet peut contenir plusieurs cibles.|

## Références

* [Comprendre le fichier de projet](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [Éléments de schéma MSBuild](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

