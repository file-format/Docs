{
  "date" : "2019-10-11",
  "keywords" :[ "fichier apng", "format de fichier apng", "qu'est-ce qu'un fichier apng", "fichier", "exemple apng", "extension de fichier apng","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier APNG - Fichier graphique réseau portable animé",
  "description":"En savoir plus sur le format de fichier APNG et les API qui peuvent créer et ouvrir des fichiers APNG.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## Qu'est-ce qu'un fichier APNG ?

Un fichier avec l'extension .apng (Animated Portable Network Graphics) est un format graphique raster et est une extension non officielle du Portable Network Graphic ([PNG](/fr/image/png/) ). Il comprend plusieurs cadres (chacun d'une image PNG) qui représente une séquence d'animation. Cela donne une visualisation similaire à un fichier [GIF](/fr/image/gif/). Les fichiers APNG prennent en charge les images 24 bits et la transparence 8 bits. APNG est rétrocompatible avec les fichiers GIF non animés. Les fichiers APNG utilisent la même extension .png et peuvent être ouverts par des applications telles que Mozilla Firefox, Chrome avec prise en charge APNG, les applications iMessage pour iOS 10.

## Bref historique

* Les spécifications APNG ont été créées en 2004 pour prendre en charge les images PNG animées
* Les décodeurs APNG ont été développés avec une taille beaucoup plus petite et en utilisant l'arrière du décodeur PNG
* Après des délibérations continues, une nouvelle image/apng de type MIME a été formulée tout en gardant l'extension identique à .png au lieu de .apng
* APNG a été officiellement rejeté par le groupe PNG le 20 avril 2007 en raison de son uniformité avec les images PNG tout en ayant des spécifications différentes

## Format de fichier APNG

Les fichiers APNG sont stockés sous forme de fichiers binaires sur disque et utilisent les spécifications étendues de PNG pour les images animées. La première image d'un fichier APNG est un flux PNG normal lisible par les décodeurs PNG pour l'affichage. Le format de fichier APNG suit les spécifications PNG et les données sont stockées dans des segments appelés morceaux. Cependant, APNG a introduit les nouveaux morceaux suivants :

`Animation Control Chunk (acTL)` - Indique que ce fichier est un fichier PNG animé plutôt qu'un fichier PNG normal. Il agit comme un marqueur et vient avant le bloc IDAT. Il contient également le nombre d'images et des informations sur les temps de boucle des animations

`Frame Control Chunk` - Se produit au début de chaque et des informations de métadonnées telles que les dimensions, la position, l'application de transparence et les informations de remplacement par l'image précédente ou suivante une fois qu'elle est terminée.

`Frame Data Chunk` - Stocke le contenu de la trame et commence par un numéro de séquence. Ce numéro de séquence a la même structure que le bloc IDAT de l'image par défaut.

{{< figure src="../APNG.png" alt="PNG animé - Format de fichier APNG" >}}

APNG est rétrocompatible avec PNG car les spécifications du latéral ont été conçues de telle manière qu'une application lisant un fichier PNG est censée simplement ignorer les morceaux qu'elle ne comprend pas. Les spécifications concernant la profondeur de bits, le type de couleur, la compression, les filtres, les méthodes d'entrelacement et les informations de palette sont utilisées de la même manière que celles du format PNG par défaut.

## APNG contre GIF

Avec le GIF déjà en place et utilisé sur une longue période, vous vous demandez peut-être en quoi APNG est différent du GIF. Voici un ensemble de comparaison entre APNG et GIF qui donne une brève idée des deux formats de fichiers.

||APNG|GIF|
---|---|---|
|Publié|2004|1987|
|Profondeur de couleur|24 bits|8 bits|
|Frame Rate|Illimité|10 images par seconde|
|Transparence|Complète et partielle|Complète|
|Compression|Très bonne|Bonne|

## Références

* [Format de fichier APNG](https://en.wikipedia.org/wiki/APNG)
* [Spécifications officielles du format PNG](https://www.w3.org/TR/PNG/)

