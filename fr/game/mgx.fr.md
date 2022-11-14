{
  "date" : "2021-09-08",
  "keywords" :[ "fichier mgx", "format de fichier mgx", "qu'est-ce qu'un fichier mgx", "fichier", "exemple mgx", "extension de fichier mgx","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier Age of Empires 2 Expansion Replay MGX et les API qui peuvent créer et ouvrir des fichiers MGX.",
  "title" :"MGX - Replay de l'extension Age of Empires 2",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Qu'est-ce qu'un fichier MGX ?

Un fichier avec l'extension .mgx est un fichier enregistré pour le jeu Age of Empires II : The Conquerors qui peut être rejoué dans le programme Age of Empires II. Il contient l'enregistrement complet de la campagne jouée par l'utilisateur. Il peut être chargé et lu dans le programme Age of Empires II. Une fois rejoué, le jeu affiche tous les événements et scénarios que l'utilisateur a planifiés pour la campagne et joués.

## Format de fichier MGX - Plus d'informations

Le format de fichier interne du fichier MGX a été élaboré et disponible en tant qu'informations partiellement validées sur [Age of Empires 2 : The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx- format). Les spécifications décrivent les détails dans les sections suivantes.

### Définitions des structures

On pense que les définitions de structure du format de fichier GPX sont basées sur les [déclarations BinData Ruby Gem](https://github.com/dmendel/bindata/wiki) qui fournissent un moyen de lire et d'écrire des données binaires structurées. Cela permet au programmeur de spécifier le format des données binaires qui sont ensuite lues et écrites par BinData.

### Messagerie MGX

La messagerie MGX est basée sur deux types de messages.

* GAMESTART - spécifie les commandes de démarrage du jeu et n'est pas validé à ce jour
* CHAT - décrit les messages de chat en jeu. Les joueurs et le jeu lui-même (Gaia) peuvent émettre des messages dans le jeu.

### ACTIONS DE JEU

Il y a plusieurs [Actions GAMEPLAY](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) qui ont été récupérées et dont les détails sont disponibles.

## Références

* [Age of Empires 2 : The Conquerors — Spécification du format de fichier de sauvegarde](https://github.com/stefan-kolb/aoc-mgx-format)

