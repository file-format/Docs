{
  "date" : "2019-10-11",
  "keywords" :[ "fichier gif", "format de fichier gif", "qu'est-ce qu'un fichier gif", "fichier", "exemple gif", "extension de fichier gif","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Format de fichier image",
  "description":"En savoir plus sur le format de fichier GIF et les API qui peuvent créer et ouvrir des fichiers GIF.",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier GIF ? ##

Un format GIF ou Graphical Interchange est un type d'image hautement compressée. Propriété d'Unisys, GIF utilise l'algorithme de compression LZW qui ne dégrade pas la qualité de l'image. Pour chaque image, le GIF autorise généralement jusqu'à 8 bits par pixel et jusqu'à 256 couleurs sont autorisées sur l'image. Contrairement à une image [JPEG](/fr/image/jpeg/), qui peut afficher jusqu'à 16 millions de couleurs et touche assez les limites de l'œil humain. À l'époque de l'émergence d'Internet, les GIF restaient le meilleur choix car ils nécessitaient une faible bande passante et étaient compatibles avec les graphiques consommant des zones de couleur unies. Un GIF animé combine de nombreuses images ou cadres dans un seul fichier et les affiche dans une séquence pour générer un clip animé ou une courte vidéo. Les limites de couleur vont jusqu'à 256 pour chaque image et sont probablement les moins appropriées pour reproduire d'autres images et photographies avec un dégradé de couleurs.

## Format de fichier GIF ##

Conceptuellement, les fichiers GIF ont une zone graphique de taille fixe remplie par zéro ou plusieurs images. Certains fichiers GIF divisent la zone graphique ou les blocs de taille fixe en sous-images capables de fonctionner comme des images animées dans le cas d'un GIF animé. Le format GIF utilise les profondeurs de pixel de 1 à 8 bits pour stocker les données bitmap. Le modèle de couleur RVB et les données de palette sont toujours utilisés pour stocker les images. Selon la version, un en-tête de longueur fixe ("GIF87a" ou "GIF89a") définit le début d'un fichier GIF typique.

Actuellement, deux versions de GIF : 87a et 89a sont disponibles. Le premier est le format GIF d'origine tandis que le second est le nouveau format GIF. Dans ce format de fichier, les caractéristiques des blocs et les dimensions en pixels sont mentionnées dans un descripteur d'écran logique de longueur fixe. L'existence et la taille d'une table de couleurs globale peuvent être spécifiées par le descripteur d'écran, qui suit d'autres détails s'ils sont présents. La fin est le dernier octet du fichier qui contient un seul octet d'un point-virgule ASCII. Une disposition de fichier GIF87a typique est la suivante :

### Entête ###

L'en-tête contient six octets et est utilisé pour spécifier le type de fichier au format GIF. Bien que le descripteur d'écran logique soit séparé de l'en-tête réel, il est parfois considéré comme le deuxième en-tête. La même structure qui est utilisée pour stocker l'en-tête peut stocker le descripteur d'écran logique. Tous les fichiers GIF commencent par la signature à 3 octets et utilisent les caractères "GIF" comme identifiant. La version a également une taille de trois octets et déclare la version du fichier GIF.

### Descripteur d'écran logique ###

Un descripteur d'image de longueur fixe spécifie les informations d'écran et de couleur nécessaires pour créer l'image GIF. Les champs Hauteur et Largeur renferment la plus petite valeur de résolution d'écran, obligatoire pour afficher les données de l'image. Si le dispositif d'affichage est incapable d'afficher la résolution spécifiée, une mise à l'échelle sera nécessaire pour afficher correctement l'image. Les informations sur l'écran et la carte des couleurs sont affichées par les quatre sous-champs du tableau ci-dessous (le bit 0 étant le bit le moins significatif) :


|Bits|Sous-champs
---|---|
|0-2|Taille de la table des couleurs globales
|3|Indicateur de tri de la table des couleurs
|4-6|Résolution des couleurs
|7|Drapeau de la table des couleurs globales

#### Table des couleurs globales ####

Une table de couleurs globale facultative est placée juste après le descripteur d'écran logique. Cette table est mappée pour indexer les données de couleur de pixel à l'intérieur des données d'image. En l'absence d'une table de couleurs globales, chaque image du fichier GIF utilise sa couleur locale. Il est préférable de fournir une table de couleurs par défaut si la table de couleurs globale et locale est manquante. Une série de triplets de trois octets compose les éléments de la table des couleurs. Chaque octet caractérise une valeur de couleur RVB. Les couleurs rouge, vert et bleu sont utilisées comme valeurs de chaque élément de la table des couleurs. Les entrées de la table des couleurs globales atteignent un maximum de 256 entrées et représentent toujours une puissance de deux.

#### Données d'image ####

Les données d'image stockent un octet de symboles non codés suivi d'une liste chaînée de sous-ensembles avec les données codées en LZW.

#### Bande annonce ####

La fin représente un seul octet de données qui est le dernier caractère du fichier. La valeur de cet octet est en permanence 3Bh et spécifie la fin du flux de données. Chaque fichier GIF doit avoir la bande-annonce dans le dernier de chaque fichier.

## Références ##

* [format de fichier GIF] (https://en.wikipedia.org/wiki/GIF)

