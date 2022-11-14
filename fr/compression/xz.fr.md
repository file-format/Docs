{
  "date" : "2022-01-23",
  "keywords" :[ "fichier xz", "format de fichier", "qu'est-ce qu'un fichier xz", "fichier", "exemple xz", "extension de fichier xz","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier XZ - Archive compressée XZ",
  "description":"En savoir plus sur le format de fichier XZ et les API qui peuvent créer et ouvrir des fichiers XZ.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## Qu'est-ce qu'un fichier XZ ?

XZ est un format de fichier compressé qui utilise l'algorithme de compression LZMA2. Il a été conçu pour remplacer les formats populaires gzip et bzip2 et offre un certain nombre d'avantages par rapport à ces anciennes normes. Les fichiers XZ sont bien pris en charge sur de nombreuses plates-formes et peuvent être décompressés rapidement et facilement. Bien qu'ils ne soient pas aussi courants que les fichiers [ZIP](/fr/compression/zip/) ou [RAR](/fr/compression/rar/), les archives XZ peuvent être utilisées pour stocker de grandes quantités de données sans sacrifier la qualité de la compression. Si vous avez besoin de compresser ou de décompresser des fichiers volumineux, l'extension de fichier XZ vaut la peine d'être envisagée.

## Format de fichier XZ

Les fichiers XZ sont générés et enregistrés sous forme de fichiers binaires sur le disque. Il utilise l'algorithme LZMA pour compresser les données et peut atteindre un taux de compression allant jusqu'à 50 %. Les fichiers XZ sont généralement utilisés pour les distributions de logiciels et les archives de sauvegarde. Ils peuvent être décompressés à l'aide de l'utilitaire XZ, inclus dans la plupart des distributions Linux.

## Décompressez les fichiers XZ sous Linux/Unix

Pour décompresser les fichiers XZ, installez d'abord le package `xz-utils` :
```
$ sudo apt-get install xz-utils
```

Utilisez la commande `unxz` pour extraire les fichiers .xz :
```
$ unxz compressed_xz_file.xz
```

ou en utilisant avec l'option --decompress de XZ :
```
$ xz --decompress compressed_xz_file.xz
```

## Références

* [Utilitaires XZ](https://en.wikipedia.org/wiki/XZ_Utils)

