{
  "date" : "2021-04-08",
  "keywords" :[ "fichier mst", "format de fichier mst", "qu'est-ce qu'un fichier mst", "fichier", "exemple mst", "extension de fichier mst","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
	

},
  "draft" : "false",
  "toc" : true,
  "title" :"LBR - Format de fichier d'archive de bibliothèque LU",
  "description":"En savoir plus sur le format de fichier LBR et les API qui peuvent créer et ouvrir des fichiers LBR.",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Qu'est-ce qu'un fichier LBR ?

Un fichier avec l'extension .lbr est un fichier d'archive créé avec le programme LU et utilisé sur les systèmes d'exploitation CP/M et DOS au cours des années 1980. Il n'est plus utilisé et a été remplacé par des formats de fichiers d'archivage modernes. Le format ne compresse pas les fichiers des membres et agit comme une archive de conteneur pour ceux-ci. La fonction d'archivage était principalement utilisée pour le transfert de fichiers archivés sur Internet. Étant donné que LBR n'offrait pas de compression, d'autres utilitaires tels que SQ ou CRUNCH ont été utilisés pour compresser le pré-archivage des fichiers membres ou le post-archivage du fichier d'archive résultant afin de réduire sa taille.

## Format de fichier LBR

Le format de fichier LBR a été conçu par Gary P. Novosielski et aucun détail technique n'est disponible publiquement. Les fichiers LBR commencent par un octet 0x00, suivi de 11 espaces (0x20), puis de deux octets 0x00, puis de deux octets qui ne sont pas tous les deux 0x00. Étant un format de fichier conteneur, il peut être extrait à l'aide de LU.COM et NULU.COM.

## Références

* [LBR - Wikipédia](https://en.wikipedia.org/wiki/LBR_(file_format))

