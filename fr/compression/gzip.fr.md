{
  "date" : "2022-06-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier GZIP - Fichier d'archive compressé GNU",
  "description":"Découvrez ce qu'est un fichier GZIP et les API qui peuvent créer et ouvrir des fichiers GZIP.",
  "linktitle" : "GZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-26"
}

## Qu'est-ce qu'un fichier GZIP ?

Un fichier GZIP est une archive compressée créée avec l'algorithme de compression standard [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). L'archive compressée peut contenir plusieurs fichiers, y compris des fichiers compressés, des répertoires et des souches de fichiers. La plupart des systèmes Unix incluent l'utilitaire de compression open source gzip (GNU Zip) pour la compression/décompression des fichiers. Les fichiers GZIP peuvent être ouverts avec des applications telles que [WinZip](https://www.winzip.com/en/).

## Format de fichier GZIP - Plus d'informations

GZIP utilise l'algorithme [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) pour compresser les fichiers en archives. Deux RFC, [RFC1952](https://tools.ietf.org/html/rfc1952) et [RFC 1951](https://tools.ietf.org/html/rfc1951), définissent les spécifications du format de wrapper gzip et dégonfler le format de données compressées, respectivement.

Les fichiers GZIP sont souvent enregistrés au format de fichier [GZ](/fr/compression/gz/).

## Références

* [gzip](http://www.gzip.org/)
* [gzip - Wikipédia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952 : spécification du format de fichier GZIP](http://tools.ietf.org/html/rfc1952), par l'IETF
* [RFC1951](https://tools.ietf.org/html/rfc1951)

