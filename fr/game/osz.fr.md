{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier OSZ et les API qui peuvent créer et ouvrir des fichiers OSZ.",
  "title" :"Fichier OSZ - osu! Format de fichier Beatmap",
  "linktitle" : "OSZ",
  "menu" : {
    "docs" : {
      "identifier":"game-osz",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Qu'est-ce qu'un fichier OSZ ?

Un fichier OSZ est un format de fichier compressé utilisé par le jeu de rythme osu ! pour stocker des données de beatmap. Les beatmaps sont essentiellement des niveaux pour le jeu, et ils incluent des informations telles que la chanson, le rythme des battements et le placement des objets touchés sur l'écran de jeu. Les fichiers OSZ permettent une distribution facile des beatmaps et sont généralement téléchargés depuis Internet et importés dans le jeu. OSU ! a également le format de fichier [OSR](/fr/game/osr/) qui est un fichier de relecture de jeu et peut être rejoué par les joueurs.

**Type MIME du format de fichier OSR :** x-osu-replay

## Format de fichier OSZ

Les détails du format de fichier interne des types de fichiers OSZ ne sont pas disponibles publiquement. Il contient des données compressées [ZIP](/fr/compression/zip/) contenant des informations permettant de lire de la musique, d'afficher des graphiques et d'afficher les joueurs sur les événements lorsqu'ils doivent interagir avec le jeu.

## Comment créer un fichier OSZ ?

OSU ! a des instructions détaillées pour [créer OSZ](https://osu.ppy.sh/wiki/en/Client/File_formats#creating-.osz-and-.osk-files
) et les fichiers OSK. Les étapes suivantes peuvent être utilisées pour créer un fichier OSZ à l'aide d'OSU!.

1. Ouvrez une beatmap via l'éditeur.
1. Dans le menu du haut, sélectionnez Fichier > Exporter le package....
1. L'archive .osz sera placée dans le dossier Exports à l'intérieur de l'osu! dossier.

## Références

* [OSU ! Jeu de rythme](https://osu.ppy.sh/home)
* [Format de fichier OSZ](https://osu.ppy.sh/wiki/en/Client/File_formats/Osz_%28file_format%29https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format %29#types-de-données)

