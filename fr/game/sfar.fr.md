{
  "date" : "2021-10-20",
  "keywords" :[ "fichier sfar", "format de fichier sfar", "qu'est-ce qu'un fichier sfar", "fichier", "exemple sfar", "extension de fichier DLC Mass Effect 3","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier SFAR de Mass Effect 3 et les API qui peuvent créer et ouvrir des fichiers SFAR.",
  "title" :"SFAR - Fichier DLC Mass Effect 3",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Qu'est-ce qu'un fichier SFAR ?

Un fichier avec l'extension .sfar est un fichier de données de jeu utilisé par Mass Effect 3 pour stocker son DLC (contenu téléchargeable) dans une archive compressée et propriétaire. Mass Effect 3 est un jeu créé par Electronic Arts, une société de développement de jeux de premier plan. Le contenu DLC stocké dans un fichier SFAR est utilisé pour étendre le jeu avec du contenu et des fonctionnalités supplémentaires.

## Format de fichier SFAR - Plus d'informations

Les fichiers SFAR sont stockés/enregistrés sous forme de fichiers d'archive compressés au format de fichier binaire. Ceux-ci utilisent à la fois les algorithmes de compression LZX et LZMA pour compresser le contenu. Les fichiers SFAR peuvent être ouverts à l'aide de l'éditeur DLC fourni avec ME3 Explorer. En plus de SFAR, DLC Editor peut extraire d'autres fichiers de jeu tels que [PCC](/fr/game/pcc/).

## Spécifications du format de fichier SFAR

Un fichier SFAR est divisé en quatre blocs principaux suivants.

### En-tête SFAR

L'en-tête SFF contient des informations sur les différents morceaux qui composent le fichier.

### Table de fichiers SFAR

La table de fichiers SFAR contient une liste d'entrées de fichier où chaque entrée a une longueur de 30 octets.

### Table de taille de bloc

La taille de bloc contient plusieurs entrées, chaque entrée ayant une longueur de 2 octets. Cette valeur spécifie la taille de bloc correspondant à une entrée dans la table de fichiers.

### Blocs

Les blocs de blocs dans un fichier SFAR contiennent les données à l'intérieur du fichier SFAR.

## Références

* [Format de fichier DLC SFAR - Recherche](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

