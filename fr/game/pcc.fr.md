{
  "date" : "2021-09-08",
  "keywords" :[ "fichier pcc", "format de fichier pcc", "qu'est-ce qu'un fichier pcc", "fichier", "exemple pcc", "extension de fichier pcc","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier Mass Effect PCC et les API qui peuvent créer et ouvrir des fichiers PCC.",
  "title" :"PCC - Fichier de package Mass Effect",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Qu'est-ce qu'un fichier PCC ?

Un fichier avec .pcc est un fichier [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) qui contient des données de jeu pour modifier le contenu du jeu tel que des modèles, des textures et pièces. Mass Effect 2 et 3 sont les premiers jeux de tir basés sur le moteur de jeu Unreal Engine 3. Le jeu a été initialement développé par [Bioware](https://www.bioware.com/about/) qui a conservé la majorité des ressources du jeu dans son format de fichier propriétaire PCC. Bioware a été acquis par Electronic Arts, l'un des principaux éditeurs mondiaux de divertissement interactif.

## Format de fichier PCC - Plus d'informations

Les fichiers PCC contiennent des structures compressées et/ou non compressées qui contribuent à l'organisation globale des fichiers.

### Structure PCC compressée

Un fichier PCC compressé comprend des tables et des données segmentées en morceaux. Chaque bloc contient un nombre variable de blocs compressés.

* `Chunks Header` - Un en-tête commun de 16 octets, contenant des informations sur les morceaux.
* `Chunk Header` - Un en-tête de 16 octets contenant des informations sur les données brutes compressées contenues dans le bloc.

### Structure PCC non compressée

Les fichiers PCC non compressés sont divisés en cinq parties.

* `Header` - contient des informations de base sur la structure du fichier PCC.
* `Name Table` - contient le nom trouvé dans le package, y compris les classes d'importation, les exportations et les propriétés d'exportation.
* `Table d'importation` - contient toutes les classes et tous les objets importés par le PCC.
* `Table d'exportation` - contient tous les objets stockés dans le package. Chaque exportation peut varier en taille.

## Références

* [Me3Explorer - Format de fichier PCC](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Jeu Mass Effect](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)

