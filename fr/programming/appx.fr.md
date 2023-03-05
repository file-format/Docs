{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - Qu'est-ce qu'un fichier APPX ?",
  "description":"En savoir plus sur le format de fichier APPX et les API qui peuvent créer et ouvrir des fichiers APPX.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Qu'est-ce qu'un fichier APPX ?

Un fichier APPX est un format de fichier de package distribuable utilisé pour la distribution et l'installation d'une application. Il a été introduit avec Windows 8 pour être publié sur Microsoft Windows Store. Il contient tous les fichiers nécessaires à l'installation d'une application Windows. Il s'agit notamment des métadonnées, des fichiers et des informations d'identification. Un format de fichier d'empaquetage plus moderne est MSIX qui est actuellement plus couramment utilisé par rapport à APPX.

## Format de fichier APPX - Plus d'informations

Les fichiers APPX sont enregistrés sous forme de fichiers compressés au format de fichier [ZIP](/fr/compression/zip/). Cela transforme l'ensemble du package en un fichier d'archive avec une taille de fichier réduite facile à télécharger sur le Microsoft Store.

## Comment afficher les fichiers dans un fichier APPX ?

Pour afficher le contenu ou les fichiers dans un fichier APPX, les étapes suivantes doivent être suivies.

1. Étant donné que les fichiers APPX sont stockés sous forme de fichiers ZIP compressés, renommez le fichier en extension .zip
1. Utilisez n'importe quel outil de décompression tel que 7-Zip, WinZip ou WinRAR pour extraire les fichiers contenus dans le fichier APPX

## Comment créer un fichier APPX ?

Deux méthodes peuvent être utilisées pour créer des fichiers APPX.

1. Utilisation de MakeApp.exe - [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) est utilisé pour créer les deux packages d'application (.msix ou .appx) et fichiers de package d'application .msixbundle ou .appxbundle). De plus, il peut extraire des fichiers d'un package d'application. MakeApp.exe est disponible avec le SDK Windows 10 et peut être utilisé à partir de l'invite de commande.
1. Utilisation de Microsoft Visual Studio - Les développeurs [créent généralement des fichiers APPX](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) à l'aide de Microsoft Visual Studio. Une fois le développement de l'application terminé et l'application prête à être publiée, le fichier de package APPX peut être créé en le publiant à partir de Visual Studio.

## Références

* [Créer un package ou un bundle MSIX avec MakeAppx.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Créer des fichiers APPX à l'aide de Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

