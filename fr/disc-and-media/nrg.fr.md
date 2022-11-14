{
  "date" : "2021-08-16",
  "keywords" :[ "fichier nrg", "format de fichier nrg", "qu'est-ce qu'un fichier nrg", "fichier", "exemple nrg", "extension de fichier nrg","extension", "format", "pied de page nrg", "fichier format de nrg", "Nero Burning Rom", "Nero AG" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"En savoir plus sur le format de fichier NRG et les API qui peuvent créer et ouvrir des fichiers NRG.",
  "title" :"NRG - Format de fichier d'image disque",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## Qu'est-ce qu'un fichier NRG ?

Un format de fichier image créé à l'aide d'un disque optique est considéré comme un format de fichier NRG. Ce format est spécifiquement créé par Nero pour l'utilitaire de Nero Burning Rom. Pour le stockage des images de disque, ce format est considéré comme étant utilisé car il est approprié pour ces fichiers spécifiques. Ces fichiers peuvent se présenter sous la forme d'une copie exacte d'un CD ou d'un DVD ou peuvent contenir plusieurs fichiers pouvant être montés sur un disque. D'autres formats de fichiers plus populaires tels que les formats de fichiers [ISO](/fr/compression/iso/) sont ceux dans lesquels ces fichiers peuvent être convertis en certains utilitaires de base. Généralement, les fichiers NRG sont utilisés pour créer des sauvegardes ou des copies de certaines données ou disques importants.

## Format de fichier NRG ##

Ce format de fichier a été développé par Nero AG en tant que format d'image disque. Il avait la propriété spécifique de l'utilitaire Nero Burning Rom car il a été développé pour stocker des images de disque. Sa première version a été spécifiée pour stocker les valeurs sous forme d'entiers 32 bits. Cependant, sa deuxième version a été lancée et contenait la prise en charge des entiers 64 bits.

## Spécifications techniques ##

Au début du fichier, ce format ne stocke pas ses données sous forme d'en-tête. Comme un pied de page, il est attaché à la fin du fichier. Sous forme de morceaux d'IFF, les informations de l'image sont stockées. Le décalage du premier morceau peut être obtenu en lisant le pied de page NRG aux 8 derniers octets à 12 octets du fichier. Dans toutes les versions du format de fichier NRG, il existe des morceaux, DAOI, texte de CD, type de support d'informations de session, informations sur le disque, Relo et fin de la chaîne qui y sont attachés. L'ordre des octets est big-endian et toutes les valeurs entières sont non signées au moment du stockage.

### Morceaux principaux ###

#### Feuille de Cue ####

Cette feuille de repère est disponible facilement dans toutes les versions de format de fichiers NRG. Le morceau de **CUEX** désigne les blocs de concaténation de taille fixe et chacun d'eux représente le point de repère.

#### Informations DAO ####

Cette information est également présente dans toutes les versions du format NRG. Les morceaux de **DAOI** stockent les informations spécifiques pertinentes en 2 parties. Sa première partie se compose uniquement des données spécifiques à la session. Sa deuxième partie ne fait que répéter les informations grises liées au suivi et ce n'est qu'une seule fois pour chaque piste.

#### CD-texte ####

Ceci est disponible dans la deuxième version de NRG. Le morceau de **CDTX** consiste en la concaténation brute du pack CD-texte ayant 18 octets pour chacun.

#### Informations de piste étendues ####

Ceci est disponible dans toutes les versions du format de fichier de NRG. Ces blocs sont utilisés pour stocker les informations de suivi pour la piste des sessions simultanées. Ces données ne sont répétées qu'une seule fois dans le cas de chaque piste.

#### Informations sur la session ####

Ceci est également disponible dans toutes les versions du format de fichier de NRG. Les informations des blocs de session doivent être utilisées pour analyser rapidement l'image de la session, puis suivre le nombre.

#### Fin de chaîne ####

Le morceau de fin signifie les signaux qu'il n'y a plus de morceaux qui doivent être lus et cela est également disponible dans toutes les versions de NRG.


## Références ##

* [NRG - par Wikipédia](https://en.wikipedia.org/wiki/NRG_(file_format))


