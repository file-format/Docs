{
  "date" : "2019-10-11",
  "keywords" :[ "fichier bz2", "format de fichier bz2", "qu'est-ce qu'un fichier bz2", "fichier", "exemple bz2", "extension de fichier bz2","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - Format de fichier compressé",
  "description":"Apprenez à savoir ce qu'est un fichier BZ2 et les API qui peuvent créer et ouvrir des fichiers BZ2.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## Qu'est-ce qu'un fichier BZ2 ?

BZ2 sont des fichiers compressés générés à l'aide de la méthode de compression open source [BZIP2](http://www.bzip.org/), principalement sur les systèmes UNIX ou Linux. Il est utilisé pour la compression d'un seul fichier et n'est pas destiné à l'archivage de plusieurs fichiers. Cela contraste avec le format de fichier TAR sur les mêmes plates-formes qui archive plusieurs fichiers dans un seul fichier mais sans compression. Les fichiers compressés au format BZ2 peuvent être décompressés avec des applications telles que [WinZip](https://www.winzip.com/win/en/). BZIP2 utilise l'algorithme de compression Run-Length Encoding (RLE) ou [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) pour atteindre des niveaux de compression élevés.

## Format de fichier BZ2

Il n'y a pas de spécifications formelles disponibles pour ce format de fichier. Cependant, une [spécifications d'ingénierie inverse] non officielle (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) montre qu'un flux .bz2 consiste en un en-tête de 4 octets qui est suivi par zéro ou plusieurs blocs compressés. Il est immédiatement suivi d'un marqueur de fin de flux contenant un CRC de 32 bits pour le flux entier de texte en clair traité. Il n'y a pas de remplissage entre les blocs compressés et tous les blocs sont alignés sur les bits.

## Décompresser/extraire le fichier BZ2

Vous pouvez décompresser un fichier BZ2 sous Windows et Mac OS à l'aide d'un logiciel tel que WinZip. Sous Linux, la commande suivante dans le terminal.

```
bzip2 -d filename.bz2
```

## Références

* [Spécifications du format BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

