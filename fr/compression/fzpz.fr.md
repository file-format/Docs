{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier FZPZ - Fichier de pièce Fritzing",
  "description":"Découvrez ce qu'est un fichier FZPZ et les API qui peuvent créer et ouvrir des fichiers FZPZ.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## Qu'est-ce qu'un fichier FZPZ ?

Un fichier FZPZ est un composant/pièce utilisé dans une conception de circuit électronique créée avec l'application de prototypage et de conception de circuit **Fritzing**. Il s'agit d'une archive compressée qui contient un fichier [FZP](/fr/cad/fzp/) et quatre images [SVG](/fr/image/svg/) décrivant l'ensemble de la pièce en Fritzing. L'avantage d'utiliser ces fichiers est que les utilisateurs peuvent partager leurs fichiers FZPZ avec chacun du point de vue de la réutilisation. Le partage de pièces FZPZ aide à intégrer des pièces de circuit pour créer rapidement des conceptions de circuits imprimés plus grandes.

## Format de fichier FZPZ - Plus d'informations

Les fichiers FZPZ sont enregistrés sur le disque sous forme d'archives compressées [ZIP](/fr/compression/zip/). Vous pouvez renommer l'extension .fzpz en .zip et utiliser n'importe quel utilitaire de décompression standard tel que WinZIP pour extraire les fichiers de l'archive.

### Informations sur la structure du fichier FZPZ

Comme mentionné, un fichier FZPZ est un fichier d'archive qui contient plusieurs fichiers pour la représentation d'une pièce utilisée dans une carte de circuit imprimé. Le FZPZ contient les fichiers suivants :

* `Quatre fichiers SVG` - qui représentent les images de la maquette, du schéma, du PCB et des icônes de la pièce
* `Fichier FZP` - Un fichier XML contenant des informations sur les propriétés, les connecteurs et les bus de la pièce

Les fichiers sont généralement nommés comme suit.

* part.file.fzp
* svg.planche à pain.fichier.svg
* svg.icon.file.svg
* svg.pbc.fichier.svg
* svg.schematic.file.svg

## Références ##

* [Nouvelles pièces avec extension fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

