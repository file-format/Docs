{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier CR2 - Fichier image Canon Raw 2",
  "description":"En savoir plus sur le format de fichier CR2 et les API qui peuvent créer et ouvrir des fichiers CR2.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Qu'est-ce qu'un fichier CR2 ?

Un fichier CR2 (Camera RAW 2) est un fichier image RAW créé par les appareils photo numériques Canon. Il stocke les données d'image originales non traitées sans perte capturées par la caméra. Le format de fichier CR2 a été développé par Canon pour ses appareils photo numériques et peut enregistrer des images de haute qualité jusqu'à 14 bits de RVB. Cela produit des images de haute qualité avec suffisamment de place pour le post-traitement. Le format d'image CR2 a été utilisé par Canon dans ses modèles d'appareils photo 350D, 20D et 1D. Les fichiers CR2 sont des fichiers RAW et contiennent des informations de métadonnées supplémentaires telles que des informations sur l'appareil photo, des informations sur l'objectif, des informations sur le bracketing, la balance des blancs et d'autres paramètres.

## Format de fichier CR2

Les fichiers CR2 sont stockés sur la carte mémoire de l'appareil photo sous forme de fichiers binaires au format de fichier propriétaire de Canon. Le format de fichier CR2 a remplacé le format de fichier CRW initialement utilisé et a été lui-même remplacé par le format de fichier Canon RAW 3 plus tard. Le format de fichier CR2 est basé sur les spécifications [TIFF](/fr/image/tiff/) qui ont 4 répertoires de fichiers d'images (IFD).

|Décalage |Contenu |Commentaire|
---|---|---|
|0x0000 |En-tête |contient l'ordre des octets, la version et le décalage par rapport à l'image RAW|
|calculé |IFD#0 |cette partie contient la section Exif, qui contient la section Makernotes.
Informations sur la photo#0|
|calculé |picture#0 |petite version de l'image (un quart de la taille de l'original), compressée en Jpeg|
|calculé |IFD#1 |Informations sur l'image#1.|
|calculé |image#1 |petite version de l'image, compressée en Jpeg|
|calculé |IFD#2 |Informations sur l'image#2.|
|calculé |image#2 |petite version de l'image, non compressée|
|dans l'en-tête| IFD#3| Informations sur l'image n ° 3, l'image RAW pleine dimension |
|calculé |image#3 |Données d'image RAW, compressées sans perte en Jpeg (pas de données RVB !)|

## Avantage du format de fichier CR2

Le stockage des images au format RAW permet de nombreux post-traitements sur la photo, tels que le réglage de la balance des blancs. C'est beaucoup plus difficile et avec une grande perte de qualité avec d'autres formats de fichiers image tels que [JPEG](/fr/image/jpeg/).

## CR2 est-il meilleur que JPEG ?

Les fichiers CR2 sont des fichiers bruts sans aucune perte de données et, par conséquent, sans perte de qualité. JPEG, d'autre part, est un format de fichier image avec perte car il perd certaines données pour réduire le fichier. Ainsi, les fichiers CR2 sont de haute qualité et plus adaptés aux retouches et améliorations.

## Références

* [Format de fichier CR2](http://lclevy.free.fr/cr2/)

