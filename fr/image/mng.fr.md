{
  "date" : "2019-10-11",
  "keywords" :[ "fichier mng", "format de fichier mng", "qu'est-ce qu'un fichier mng", "fichier", "exemple mng", "extension de fichier mng","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier MNG - Format de fichier graphique réseau à images multiples",
  "description":"En savoir plus sur le format de fichier MNG et les API qui peuvent créer et ouvrir des fichiers MNG.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier MNG ?

Un fichier avec l'extension .mng est un format de fichier Network Graphics à images multiples similaire au format d'image [PNG](/fr/image/png/) mais prenant en charge les images animées. Il a été développé pour éviter de surcharger le format PNG avec des fonctionnalités supplémentaires d'animations. MNG est également similaire aux fichiers [GIF](/fr/image/gif/) mais utilise plus de compression et prend en charge la fonctionnalité alpha complète. Le type de média MIME non officiel pour les fichiers MNG est video/x-mng. Les fichiers MNG peuvent être ouverts dans des applications telles que ImageMagik et IrfanView.

## Format de fichier MNG

Le format de fichier MNG est similaire à celui de PNG et utilise la même structure de bloc que celle définie dans les spécifications PNG. Un décodeur MNG doit être capable de décoder les flux de données PNG sans spécifier de drapeaux spéciaux pour les instructions de décodage. MNG regroupe plusieurs images dans un "cadre", certaines images étant utilisées comme sprite pour se déplacer d'un endroit à un autre. Le mécanisme permet de réutiliser les données d'image sans les retransmettre. Les [spécifications MNG](http://www.libpng.org/pub/mng/spec/) peuvent être consultées à titre de référence pour les développeurs.

### Signature MNG

Le flux de données MNG commence par une signature de 8 octets contenant :

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Ceci est similaire à celui de la signature PNG mais contient MNG au lieu de PNG.

### Cadre MNG

Un cadre MNG consiste en une image bidimensionnelle d'images plus petites. Chaque petite image est accessible à l'aide de la combinaison d'index de ligne et de colonne. Le format est capable de stocker des données "voxel" tridimensionnelles qui sont agencées en une série de plans bidimensionnels. Chaque plan est représenté par un flux de données PNG ou Delta-PNG. Chaque flux de données Delta-PNG définit une image comme les différences par rapport à l'image PNG parente. Cela fournit un moyen beaucoup plus compact de représenter les images suivantes que d'utiliser un flux de données PNG complet pour chacune.

## Références ##

* [MNG](http://www.libpng.org/pub/mng/)
* [Format MNG v 1.0](http://www.libpng.org/pub/mng/spec/)

