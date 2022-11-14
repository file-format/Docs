{
  "date" : "2021-06-16",
  "keywords" :[ "LZH", "Compressé", "Fichier", "Extension", "Format de fichier", "Lempel-Ziv", "Haruyasu", "LHA" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier LZH",
  "description":"En savoir plus sur le format de fichier LZH et les API qui peuvent créer et ouvrir des fichiers LZH.",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Qu'est-ce qu'un fichier LZH ? ##

Un fichier avec l'extension .lzh et .lha se rapporte généralement au format de fichier de compression d'archive. Ce format de fichier est le même que d'autres formats de compression de fichiers tels que [ZIP](/fr/compression/zip/), [RAR](/fr/compression/rar/), etc. L'objectif principal de ces formats de fichiers est de réduire la taille du format pour les envoyer facilement ainsi que pour les conserver ensemble sous forme compressée. Comparés à d'autres sociétés occidentales, les fichiers LZH sont très populaires au Japon et généralement utilisés pour compresser les données de jeux vidéo. Le module complémentaire LZH pour Windows 7 est intégré à la version japonaise de Windows 7. Microsoft a d'abord publié le module complémentaire de dossier compressé Microsoft (LZH) pour la version japonaise de Windows XP. Ce format de fichier est implémenté avec des dispositions de compression et des fonctionnalités utilisées par l'algorithme Lempel-Ziv et Haruyasu

## Spécification LZH ##

La méthode de compression d'une archive LZH est affichée sous la forme d'une chaîne de texte de cinq octets, telle que -lz1-. Ce sont les troisième à septième octets du fichier compressé.

|Spécification|Description|
---|---|
|Extension | .lzh, .lha|
|Type de média| application/x-lzh-compressé |
|Type Code| "LHA_" (LHA-ESPACE)|
|UTI| public.archive.lha|
|Développé par| Haruyasu Yoshizaki (Yoshi) |
|Type| Compression|
|Prolongé de| LArc|

## Problèmes pour ouvrir un fichier LZH ##

Voici les quelques problèmes qui peuvent entraîner un mauvais fonctionnement du format de fichier LZH :
  

* Le fichier peut être corrompu. Pour résoudre ce problème, téléchargez à nouveau le fichier ou demandez à l'expéditeur de renvoyer le fichier à nouveau
* La deuxième raison est le fichier infecté dans ce cas, analysez le fichier correctement
* Liens incorrects vers le fichier LZH
* Suppression de la description du LZH
* Pas assez de ressources matérielles
* Pilotes obsolètes de l'équipement

## Références ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
