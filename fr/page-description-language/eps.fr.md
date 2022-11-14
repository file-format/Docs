{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "fichier", "extension", "format de fichier", "Mise en page", "PostScript encapsulé" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier EPS et les API qui peuvent créer et ouvrir des fichiers EPS.",
  "title" :"Format de fichier EPS - Fichier PostScript encapsulé",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier EPS ?

Un fichier .eps est un fichier image enregistré sur un disque au format de fichier Postscript encapsulé. Il peut contenir n'importe quelle combinaison de texte, de graphiques et d'images. Les fichiers EPS peuvent également inclure une image d'aperçu bitmap encapsulée à l'intérieur pour être affichée par des applications pouvant ouvrir de tels fichiers.

## Bref historique du format de fichier EPS

Un rapide coup d'œil au format de fichier EPS du point de vue de l'historique révèle les informations suivantes :

* La première version d'EPS a été publiée par Adobe entre 1985 et 1988
* La version 2.0 de la spécification EPS a été publiée en janvier 1989
* La spécification de la version 3.0 d'EPS a été publiée en tant que document séparé en 1992 ; c'est la dernière version publiée.

EPS, en combinaison avec le mécanisme d'extension des conventions de structuration ouvertes décrit dans la clause 9 de la spécification des conventions de structuration des documents en langage PostScript d'Adobe, a constitué la base des premières versions du format de fichier Adobe Illustrator Artwork.

## Format de fichier EPS

EPS est un format propriétaire mais documenté publiquement et les spécifications du format de fichier EPS sont disponibles publiquement pour la référence du développeur. EPS est un format de fichier conforme [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Convention de structuration des documents) et respecte toutes les règles établies par le DSC. Le DSC est un format de fichier spécial pour les documents PostScript d'Adobe. Toute application prétendant pouvoir lire les fichiers EPS doit être compatible DSC.

Un fichier EPS se compose de deux sections principales, comme expliqué ci-dessous.

### Aperçu de l'image ###

Un fichier EPS typique contient une image d'aperçu dans un format destiné à une utilisation pratique dans un flux de travail impliquant plusieurs systèmes ou applications. L'intention d'un aperçu est d'avoir une image dans un format que la plupart des applications graphiques peuvent rendre ; un aperçu est généralement de résolution inférieure, en pixels et/ou en profondeur de bits. Le fichier d'aperçu peut être dans l'un des nombreux formats. La spécification pour EPS_3 répertorie trois formats d'aperçu "spécifiques à l'appareil" :

* pour Apple Macintosh, une image PICT telle qu'utilisée par l'application QuickDraw
* pour les ordinateurs DOS, un bitmap TIFF
* Métafichier Windows.

PICT et Windows Metafile peuvent incorporer à la fois des données bitmap et des graphiques vectoriels. De plus, la spécification définit une représentation très simple indépendante du périphérique pour une image de prévisualisation bitmap intégrée. Cette représentation est connue sous le nom de format d'échange PostScript encapsulé (EPSI).

Un aperçu EPSI est un bitmap représenté en hexadécimal ASCII, enveloppé entre quelques commentaires PostScript pour l'identification et destiné à être simple et facilement transportable. Afin de distinguer les fichiers EPS avec les différents formats d'aperçu, différentes extensions de fichiers DOS et types de fichiers Macintosh ont été recommandés dans la spécification EPS.

### Code PostScript

Au minimum, le format de fichier EPS doit inclure les éléments suivants :

* un commentaire d'en-tête, %!PS-Adobe-3.0 EPSF-3.0
* et un commentaire de cadre de délimitation, %%BoundingBox : llx lly urx ury, qui décrit les limites de l'illustration. Ces quatre arguments correspondent aux coins inférieur gauche (llx, lly) et supérieur droit (urx, ury) de la boîte englobante.

Un fichier EPS ne peut utiliser aucun des opérateurs suivants :

* appareil à bande,
* cleardictstack
* page de copie
* effacer la page
* quitter le serveur
* dispositif de cadre
* dans l'ensemble
* initclip
* initgraphics
* initmatrice
* quitter
* bandes de rendu
* setglobal
* setpagedevice
* ensemble partagé
* travail de démarrage.

## Conversion d'EPS en d'autres formats de fichiers

Les fichiers EPS peuvent être convertis en formats d'image standard tels que [JPG](/fr/image/jpeg/), [PNG](/fr/image/png/), [TIFF](/fr/image/tiff/) et [PDF](/fr/pdf /) à l'aide de différentes applications, par exemple Adobe Illustrator, Photoshop et PaintShop Pro.

En raison d'une [vulnérabilité de sécurité](https://support.office.com/en-us/article/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e- a1b5-cbb0c334a840) dans les fichiers EPS, Office 2016, Office 2013, Office 2010 et Office 365 ont désactivé la possibilité d'insérer des fichiers EPS dans des documents Office.

## Références

* [PostScript encapsulé - Par Wikipédia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

