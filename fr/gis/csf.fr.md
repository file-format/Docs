{
  "date" : "2023-01-27",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier CSF - Format de fichier du système de coordonnées GeoMedia",
  "description":"Découvrez le format de fichier CSF et les API permettant de créer et d'ouvrir des fichiers CSF.",
  "linktitle" : "CSF",
  "menu" : {
    "docs" : {
      "identifier":"gis-csf",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-27"
}

## Qu'est-ce qu'un fichier CSF ?

Un fichier CSF est un fichier de système de coordonnées qui contient des informations sur le système de coordonnées d'un fichier SIG. Il est utilisé par le logiciel GeoMedia d'Intergraph pour définir les paramètres d'un système de coordonnées particulier. Ceux-ci incluent des paramètres d'information tels que les données, la projection et les unités de mesure. Ces informations sont utilisées pour produire des cartes pour les données de sortie qui n'ont pas de système de coordonnées en place. Ces informations sont utilisées par GeoMedia pour afficher et manipuler correctement les données géographiques dans le système de coordonnées correct.

## Format de fichier CSF

Les fichiers CSF sont stockés sous forme de fichier texte avec les détails du système de coordonnées géographiques. GeoMedia permet d'importer des fichiers d'informations géographiques à partir de données d'entrée pour lesquelles aucun système de coordonnées n'est défini. À l'aide du système de projection et de coordonnées, les systèmes SIG affichent le fichier cartographique avec des valeurs exactes. Un fichier CSF est créé au même emplacement que le fichier de sortie.

## Les références

* [Comment afficher ou diffuser correctement les données de fichiers de formes dans GeoMedia ?](https://supportsi.hexagon.com/help/s/article/How-do-you-correctly-display-or-serve-shapefile-data-into?language=en_US)

