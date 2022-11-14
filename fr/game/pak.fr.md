{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "format de fichier", "qu'est-ce qu'un fichier pak", "fichier", "exemple de pak", "Fichier de package de jeu vidéo","extension"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le fichier .pak et les API qui peuvent créer et ouvrir des fichiers PAK.",
  "title" :"Format de fichier PAK - Fichier de package de jeu vidéo",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Qu'est-ce qu'un fichier PAK ?

Un fichier PAK est un fichier de package créé par différents jeux vidéo pour archiver les données du jeu. Il s'agit essentiellement d'un format de fichier de jeu. Cela peut inclure plusieurs éléments de jeu tels que des graphiques, des textures, des sons, des objets, ainsi que d'autres données de jeu. L'archive est principalement enregistrée sous forme de fichier .zip et peut être extraite avec des logiciels de décompression populaires tels que WinZip et WinRAR. Quake, Hexen, Crysis et Half-Life sont des exemples de jeux vidéo utilisant des fichiers PAK.

## Format de fichier PAK - Plus d'informations

Dans la plupart des cas, les fichiers PAK sont enregistrés au [format de fichier ZIP](/fr/compression/zip/). Mais différentes applications peuvent utiliser un format de fichier différent pour stocker ces fichiers.


## Comment ouvrir les fichiers PAK ?

Vous pouvez ouvrir des fichiers PAK avec des applications telles que [PakExplorer](https://www.quaketerminus.com/tools.shtml) et [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------------------ -------------------------------------------------- ------------------------**

## Format de fichier PAK - Fichier objet Simutrans

Un fichier avec l'extension .pak est un format de fichier de jeu de simulation de transport [Simutrans](https://www.simutrans.com/en/). Il contient des objets utilisés dans la simulation tels que des graphiques créés par l'utilisateur et le contenu des données. Il peut avoir plusieurs objets différents tels que des véhicules de jeu, des bâtiments, un terrain, etc. Les fichiers PAK sont générés à l'aide de MakeObject, un utilitaire qui compile des fichiers .dat et des images .png pour créer ces objets de simulation. Simutrans permet aux joueurs de gérer un système de transport réussi en construisant et en gérant des systèmes de transport de passagers, de courrier et de marchandises par voie terrestre

## Comment créer des fichiers PAK ?

Simutrans a répertorié des exemples d'exemples de création de fichiers PAK sur les systèmes d'exploitation Windows et Linux.

### Système d'exploitation Windows

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## Références

* https://simutrans-allemagne.com/wiki/wiki/en_doPak
* https://en.wikipedia.org/wiki/Simutrans

