{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier NUPKG - Fichier de package NuGet",
  "description":"En savoir plus sur le format de fichier NUPKG et les API qui peuvent créer et ouvrir des fichiers NUPKG.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## Qu'est-ce qu'un fichier NUPKG ?

Un fichier NUPKG est un fichier de package qui contient le code source à utiliser par le logiciel NuGet pour créer des packages à utiliser dans les projets .NET. Le composant NuGet Package Manager est installé dans le cadre de Microsoft Visual Studio pour récupérer des packages à partir du référentiel d'hébergement de packages en ligne. Les fichiers NUPKG aident les développeurs à récupérer les derniers packages de [Nuget.org](https://nuget.org) à l'aide du gestionnaire de packages NuGet au lieu de télécharger et d'installer manuellement les packages de développement. Les fichiers NUPKG sont créés à partir de fichiers NUSPEC et, une fois récupérés, installent le package sur le système utilisateur.

## Format de fichier NUPKG

Les fichiers NUPKG sont des archives [ZIP](/fr/compression/zip/) qui contiennent les bibliothèques empaquetées à l'intérieur. Une fois téléchargé, il peut être renommé en .zip et extrait avec n'importe quel utilitaire zip standard comme WinZIP, 7-Zip et Apple Archive Utility.

## Référence

* [Nuget.org](https://nuget.org)
* [Démarrage rapide : installer et utiliser un package dans Visual Studio (Windows uniquement)](https://docs.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- studio)
* [Comment créer et publier un package Nuget](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- cli)

