{
  "date" : "2019-10-11",
  "keywords" :[ "fichier b6z", "format de fichier b6z", "qu'est-ce qu'un fichier b6z", "fichier", "exemple b6z", "extension de fichier b6z","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"B6Z - Format de fichier d'archive B6ZIP",
  "description":"En savoir plus sur le format de fichier B6Z et les API qui peuvent créer et ouvrir des fichiers B6Z.",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Qu'est-ce qu'un fichier B6Z ?

Un fichier avec l'extension .b6z est un fichier d'archive compressé créé par une application logicielle macOS [B6Zip](http://b6zip.com) qui est utilisée pour compresser et décompresser des fichiers. Il s'agit d'un format d'archive relativement nouveau qui permet un taux de compression plus élevé. B6Z a une architecture ouverte et prend en charge des tailles de fichiers jusqu'à 900 000 Po. Il prend en charge la compression des données, la récupération des erreurs et la répartition des fichiers. Le logiciel utilitaire B6Zip est disponible gratuitement sur MacOS pour ouvrir différents types de fichiers compressés, y compris B6Z.

## Format de fichier B6Z

Le format de fichier B6Z est basé sur une architecture ouverte et fournit une compression solide avec l'algorithme de chiffrement AES-256. Il utilise LZMA2 comme méthode de compression par défaut, mais prend également en charge d'autres méthodes de compression comme suit.

|Méthode|Description|
---|---|
|LZMA |Version optimisée de l'algorithme LZ77|
|LZMA2| Version améliorée de LZMA |
|Dégonfler| Algorithme LZ77 régulier |
|BZip2| Algorithme BWT standard |
|PPMD| PPMdH de Dmitry Shkarin |

L'utilitaire B6Zip prend en charge toutes ces normes de compression et est hautement optimisé, ce qui se traduit par une vitesse élevée. Il prend en charge les formats de fichiers [ZIP](/fr/compression/zip/), [TAR](/fr/compression/tar/) et [RAR](/fr/compression/rar/). Les fichiers B6Z ont le type MIME application/x-b6z-compressed.

## Références

* [B6Zip](http://b6zip.com)

