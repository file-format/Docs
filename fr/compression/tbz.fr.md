{
  "date" : "2019-10-11",
  "keywords" :[ "fichier tbz", "format de fichier tbz", "qu'est-ce qu'un fichier tbz", "fichier", "exemple tbz", "extension de fichier tbz","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Archive tar compressée Bzip",
  "description":"En savoir plus sur le format de fichier TBZ et les API qui peuvent créer et ouvrir des fichiers TBZ.",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Qu'est-ce qu'un fichier TBZ ?

Un fichier avec l'extension .tbz est une archive compressée qui utilise la compression BZIP pour réduire la taille des fichiers de contenu. Les fichiers TBZ sont en fait des fichiers archivés UNIX [TAR](/fr/compression/tar/) qui sont ensuite compressés avec BZIP. La compression de second niveau la plus récente est [BZIP2](/fr/compression/bz2/) qui a remplacé BZIP. Le format de fichier TBZ convient au transfert de fichiers volumineux. Les fichiers TBZ peuvent être ouverts/extraits à l'aide d'applications logicielles telles que 7-Zip, PeaZip et jZip. Les utilisateurs Linux et macOS peuvent également ouvrir un TBZ avec la commande BZIP2 à partir d'une fenêtre de terminal.

## Format de fichier TBZ

Les fichiers TBZ sont en fait des archives compressées créées avec la compression BZIP/[BZIP2](/fr/compression/bz2). Il n'y a pas de spécifications formelles disponibles pour ce format de fichier. Cependant, une [spécifications d'ingénierie inverse] non officielle (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) montre qu'un flux .bz2 consiste en un en-tête de 4 octets qui est suivi par zéro ou plusieurs blocs compressés.

## Références ##

* [Spécifications du format BZIP2] (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

