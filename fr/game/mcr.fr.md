{
  "date" : "2022-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier MCR et les API qui peuvent créer et ouvrir des fichiers MCR.",
  "title" :"MCR - Format de fichier de région Minecraft",
  "linktitle" : "MCR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2022-12-14"
}

## Qu'est-ce qu'un fichier MCR ?

Le format de fichier Minecraft MCR est un format de données utilisé par Minecraft pour stocker des morceaux de terrain d'un monde Minecraft. Il est basé sur le format NBT (Named Binary Tag), qui a été développé par les développeurs du populaire moteur de jeu open source, Minecraft Forge. Le type de fichier MCR a été introduit au tout début et a ensuite été remplacé par le [format de fichier MCA](/fr/game/mca/).

## Format de fichier MCR

Le format de fichier MCR est structuré comme une série de balises binaires nommées, chacune contenant un type spécifique de données. La balise de niveau supérieur est la balise "Level", qui contient toutes les données d'un seul niveau de jeu. Dans la balise Level, il existe plusieurs autres balises nommées qui stockent différents types de données, telles que la balise "Data", qui stocke des informations sur le monde du jeu, et les balises "Entities" et "TileEntities", qui stockent des données sur le objets de jeu et entités de tuiles dans le monde, respectivement.

## Qu'y a-t-il dans le format de fichier MCR ?

Dans le format de fichier Minecraft MCR, une région est une zone de bloc 32x32 du monde du jeu. Le format MCR divise le monde du jeu en régions afin de gérer les données plus efficacement et de permettre un chargement et une sauvegarde plus rapides des niveaux de jeu. Chaque région est stockée dans un fichier séparé et le format de fichier MCR utilise un système de coordonnées pour identifier la position de chaque région dans le monde du jeu. Les coordonnées d'une région sont déterminées par les coordonnées de bloc du coin inférieur gauche de la région. Par exemple, une région avec des coordonnées (-1,0) serait située une région à gauche et zéro région en dessous de l'origine du monde du jeu.

## Spécifications du format de fichier MCR

Les spécifications du format de fichier MCR sont accessibles au public. Les spécifications du format NBT, sur lesquelles repose le format MCR, sont disponibles sur le site Web de Minecraft Forge. De plus, le [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) contient également des informations détaillées sur le format de fichier MCR, y compris sa structure et les différents types de données qu'il prend en charge.

### Données compressées dans les fichiers MCR

Le format de fichier Minecraft MCR prend en charge la compression. Le format de fichier MCR est basé sur le [format NBT](https://minecraft.fandom.com/wiki/NBT_format) qui permet de stocker les données sous une forme compressée. Cela permet de réduire la taille des fichiers MCR et de les rendre plus efficaces à transférer et à stocker. Il s'agit d'une caractéristique importante du format de fichier MCR, car il permet aux joueurs de partager de grandes données de terrain Minecraft World avec d'autres.

## Références

* [Éditeur mondial pour Minecraft](https://www.mcedit.net/)
* [À propos de Minecraft](https://www.minecraft.net/en-us)
* [Format de fichier de région](https://minecraft.fandom.com/wiki/Region_file_format)
* [Format NBT](https://minecraft.fandom.com/wiki/NBT_format)

