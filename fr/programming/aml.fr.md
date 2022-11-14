
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier AML - Fichier de langage de balisage d'assistance Microsoft",
  "description":"Découvrez ce qu'est un fichier AML et les API qui peuvent créer et ouvrir des fichiers AML.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML - Fichier de langage de balisage d'assistance Microsoft

## Qu'est-ce qu'un dossier AML ?

Un fichier AML (Assistance Markup Language) est un fichier XML généré avec Microsoft Assistance Markup Language (MAML). Il a été développé par Microsoft pour fournir une aide en ligne pour le système d'exploitation Microsoft Windows. Auparavant, l'aide de Windows était disponible au format de fichier HTML compilé [CHM](/fr/web/chm/). Les fichiers AML fournissent un document structuré qui permet à l'application de créer du code source et des pages d'aide. Cela permet de définir les documents et leurs éléments constitutifs par leur contexte. Les fichiers d'aide AML sont publiés en ligne et peuvent être configurés pour être mis à jour à partir des mises à jour de packages disponibles en ligne.

## Structure des fichiers MAML

Les fichiers AML générés à l'aide de MAML sont enregistrés en tant que fichiers [XML](/fr/web/xml/) qui peuvent être utilisés pour exprimer un large éventail de concepts actifs. Il peut également fournir une aide guidée (assistant de contenu actif) qui rend le fichier d'aide interactif pour l'utilisateur avec un assistant étape par étape.

Un fichier AML généré à l'aide de MAML suit sa structure de création qui peut être divisée en segments comme :

* Conceptuel
* FAQ
* Glossaire
* Procédure
* Référence
* Contenu réutilisable
* Tâche
* Dépannage, et
* Didacticiel

## Comment créer des fichiers MAML ?

Les fichiers MAML peuvent être créés à l'aide de l'une des méthodes suivantes :

* Utilisation de Sandcastle - Utilise une suite de schémas et d'exécutables de programme pour générer le fichier d'aide. Cet outil a cependant été abandonné.
* Utilisation de DocProject - Un plugin Microsoft Visual Studio qui peut être exécuté à partir de Microsoft Visual Studio pour générer le contenu de l'aide.

Les fichiers MAML peuvent être créés à l'aide de Sandcastle, une suite de schémas .XSL et d'exécutables de programme. Ils peuvent également être créés à l'aide de DocProject, un complément d'outil de création d'aide de Microsoft Visual Studio.

## Références

* [Créer une aide basée sur XML à l'aide de PlatyPS
](https://docs.microsoft.com/en-us/powershell/scripting/dev-cross-plat/create-help-using-platyps?view=powershell-7.2)
* [Langage de balisage Microsoft Assistance] (https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML - Fichier de langage macro Arc

## Qu'est-ce qu'un fichier ARC Macro AML ?

Un fichier AML (ARC Macro Language) est un fichier de script généré avec l'application SIG ArcInfo Workstation. Il est écrit dans le langage macro ARC, qui est un langage algorithmique propriétaire de haut niveau pour la création d'applications SIG dans ArcInfo. AML a été conçu par ESRI en 1986 et a servi à créer des applications à partir de leur système SIG ARCINFO en ligne de commande. En tant que fichier de script, les fichiers AML peuvent contenir des commandes de script pour effectuer un certain nombre de tâches telles que la création de composants d'interface utilisateur et la manipulation de données cartographiques.

## Format de fichier AML - Plus d'informations

AML, étant des fichiers de script, enregistrez les informations sur le disque sous forme de fichiers texte brut. Il suit la syntaxe AML qui était basée sur le langage shell CPL du système d'exploitation PRIMOS. Le langage AML a été remplacé par le cadre de géotraitement d'ESRI qui fait partie de la suite ArcGIS et utilise ArcObjects pour fournir un support de programmation via VBA ou Python.

## Références

* [Langage macro ARC] (https://en.wikipedia.org/wiki/ARC_Macro_Language)
* [Utilisation d'AML avec des outils de script](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

