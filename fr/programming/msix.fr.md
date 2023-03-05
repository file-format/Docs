{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - Qu'est-ce qu'un fichier MSIX ?",
  "description":"En savoir plus sur le fichier MSIX et les API qui peuvent créer et ouvrir des fichiers MSIX.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Qu'est-ce qu'un fichier MSIX ?

Un fichier MSIX est un format de package d'application Windows utilisé pour créer et distribuer des applications dans Windows 10. Il s'agit du format de fichier de package moderne par rapport à [APPX](/fr/programming/appx/) et MSI qui seront finalement supprimés. à ce nouveau format de fichier. Il peut être utilisé pour le déploiement d'applications Win32, WPF et Windows Forms. Les fichiers MSIX sont fiables et ciblent l'optimisation du réseau et de l'espace disque. Les développeurs les utilisent pour distribuer des programmes aux utilisateurs finaux via le Microsoft Store (anciennement Windows Store).

## Format de fichier MSIX - Plus d'informations

Les fichiers MSIX sont compressés [ZIP](/fr/compression/zip/), avec tous les fichiers inclus dans le fichier empaqueté. Outre les fichiers liés à l'application, le fichier MSIX contient des fichiers de configuration [.xml](/fr/web/xml/) qui contiennent des informations relatives à l'installation de l'application.

## Que contient un package MSIX ?

Un package MSIX se compose des fichiers suivants.

* `AppxBlockMap.xml` - Connu sous le nom de fichier de carte de bloc de package, il s'agit d'un document XML qui contient une liste de fichiers d'application avec des index et des hachages cryptographiques pour chaque bloc de données stocké dans le package.
* `AppxManifest.xml` - Un document XML qui contient les informations requises pour le déploiement, l'affichage et la mise à jour d'une application MSIX. Ces informations incluent l'identité du package, les dépendances du package, les fonctionnalités requises, les éléments visuels et les points d'extensibilité.
* `AppxSignature.p7x` - Un fichier généré lorsque le package est signé. Tous les packages MSIX doivent être signés avant l'installation. Avec AppxBlockmap.xml, la plateforme est capable d'installer le package et d'être validée.

## Références

* [Présentation de MSIX](https://docs.microsoft.com/en-us/windows/msix/overview)
* [Créer des fichiers APPX à l'aide de Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

