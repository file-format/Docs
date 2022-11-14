{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :[ "SWF", "fichier", "extension", "format", "format vidéo","Qu'est-ce qu'un fichier SWF", "format de fichier swf", "lecteur de fichier swf","comment ouvrir un fichier swf"] ,
  "title" :"Fichier SWF - Format de fichier vidéo Shockwave Flash",
  "description":"Découvrez ce qu'est un fichier SWF et les API qui peuvent créer et montrer comment ouvrir le fichier SWF.",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier SWF ?

Un fichier SWF est un fichier d'animation créé avec Adobe Flash. Il peut contenir différents types d'éléments tels que du texte, des images vectorielles, des images raster, des scripts d'action, des objets tels que des cercles, des lignes, des carrés et des rectangles pour créer l'animation. Les fichiers SWF organisent ces éléments multimédias dans des images qui peuvent être lues sur différentes images par seconde (fps). SWF signifie Short Web File mais est également connu sous le format Shockwave.

Les applications qui pouvaient * ouvrir les fichiers SWF ** comprenaient Adobe Flash Player (maintenant abandonné) et Eltima Elmedia Player.

## Format de fichier SWF - Plus d'informations

Les fichiers SWF étaient utilisés pour être stockés sous forme de fichiers binaires sur disque. Le format de fichier SWF a été utilisé pour développer des animations et des jeux pouvant être intégrés dans des sites Web et joués indépendamment. Il prenait également en charge les vidéos et les sons qui offraient aux développeurs de nombreux choix pour créer des applications multimédias interactives. Les fichiers SWF peuvent être lus dans les navigateurs Web sur lesquels Adobe Shockwave est installé. Adobe Flash a été abandonné en décembre 2020 en raison de ses lacunes et de problèmes de sécurité.

## Bref historique du format de fichier SWF

Le format de fichier SWF a été conçu à l'origine par FutureWave Software, pour afficher des animations avec l'intention de s'exécuter sur un logiciel de lecture sur n'importe quel système avec des connexions réseau plus lentes, tout en gardant une petite taille de fichier. En décembre 1996, Macromedia était propriétaire de FutureWave et converti en Macromedia Flash 1.0.

En 2005, Macromedia a été racheté par Adobe, qui a annoncé le SWF dans le cadre de son projet open source en 2008. Au cours de la même année, Adobe a publié du code pour les moteurs Web les plus populaires au monde afin de leur permettre d'explorer et d'indexer les fichiers SWF. Cependant, comme les fichiers SWF semblent devenir un format standard pour la publication de contenu Flash sur Internet, le SWF a été révisé pour signifier Small Web Format.

## Structure des fichiers SWF

Le chemin est l'élément graphique de base dans SWF, qui est une séquence de segments d'éléments de base, allant de simples lignes à des courbes de Bézier. Ces éléments simples aident également à créer d'autres primitives supplémentaires comme des cubes, des ellipses et même des textes. Les primitives graphiques de SWF présentent des similitudes avec les éléments graphiques d'autres formats tels que SVG et MPEG-4 BIFS.

L'affichage de listes et la réutilisation/renommage d'éléments déjà définis sont également autorisés par le format. Le format de flux binaire de SWF peut être comparé aux atomes QuickTime qui sont similaires en termes de balise, de taille et de charge utile. Le format de flux binaire permet aux lecteurs plus anciens d'ignorer les contenus non pris en charge. Bien que les versions originales de SWF aient été limitées pour offrir des graphiques et des images vectoriels, les nouvelles versions autorisent également les contenus audio et vidéo.

Une nouvelle API 3D de bas niveau de Flash Player nommée "Stage3D" a été introduite dans la version 11. Cette API a été envisagée pour être la contrepartie d'OpenGL ou de Direct3D. Stage3D définit les couleurs dans un langage de bas niveau appelé Adobe Graphics Assembly Language (AGAL). Voici quelques types de données de base du format de fichier SWF.

### Coordonnées

Les coordonnées XY au format de fichier SWF sont stockées sous forme de nombres entiers et mesurées dans une unité appelée twip. Un twip consiste en 1/20e de pixel logique. Le pixel logique et le pixel d'écran sont les mêmes lorsque le fichier est lu sans mise à l'échelle à 100 %.

### Types entiers et ordre des octets

Les types d'entiers signés et non signés de 8, 16, 32 et 64 bits sont autorisés dans le format de fichier SWF. L'ordre des octets petit-boutien est utilisé pour stocker les valeurs entières. Bien que dans les octets, l'ordre des bits est stocké en big-endian. Toutes les valeurs entières doivent être alignées sur les octets. Les entiers signés sont représentés à l'aide de modèles de bits traditionnels en complément à 2.

### Nombres à virgule fixe

Deux types de nombres à virgule fixe sont pris en charge par le format de fichier SWF, à savoir 32 et 16 bits.

### Nombres à virgule flottante

SWF 8 et les versions ultérieures utilisent trois types de nombres à virgule flottante (FLOAT, FLOAT 16, DOUBLE) qui sont compatibles avec la norme IEEE 754 des types à virgule flottante.

### Entiers codés

Un type d'entier codé est pris en charge par SWF 9 et versions ultérieures avec un nombre variable d'octets.

## Références

* [format de fichier SWF](https://en.wikipedia.org/wiki/Swf)

