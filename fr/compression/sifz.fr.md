{
  "date" : "2021-04-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier SIFZ - Fichier de projet compressé Synfig Studio",
  "description":"En savoir plus sur le format de fichier SIFZ et les API qui peuvent créer et ouvrir des fichiers SIFZ.",
  "linktitle" : "SIFZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-30"
}

## Qu'est-ce qu'un fichier SIFZ ?

Un fichier SIFZ est un fichier SIF compressé gzip créé par l'application open source de création d'animations 2D **Synfig Studio**. Il contient plusieurs éléments graphiques qui composent l'animation. Le contenu global de l'animation est construit à l'aide d'une combinaison d'un canevas rempli de formes, de coups de pinceau ou de crayon et de texte. Tous ces éléments sont disposés selon leurs propres positions, rayon, tangente, angle, sommet et poignées de largeur. Les fichiers SIFZ peuvent être ouverts avec [Synfig Studio](https://www.synfig.org/).

## Format de fichier SIFZ

Les fichiers SIFZ sont des fichiers [ZIP](/fr/compression/zip/) compressés qui sont empaquetés à l'aide de la méthode de compression gzip. Synfig est utilisé pour créer des animations de qualité cinématographique à l'aide d'illustrations vectorielles et bitmap. Contrairement à l'ancienne méthode de création d'animation image par image, elle vous permet de produire des animations 2D de meilleure qualité avec moins de ressources.

Les fichiers SIFZ, étant compressés, sont plus petits que les fichiers SIF non compressés. Cela facilite également le transfert sur des connexions Internet à faible bande passante.

## Références

* [Synfig Open Source - Github](https://github.com/synfig/synfig/)
* [Documentation Synfig](https://synfig.readthedocs.io/en/latest/index.html)

