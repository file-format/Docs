{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - Format de grille binaire ESRI ArcInfo",
  "description":"En savoir plus sur le format de fichier ADF et les API qui peuvent créer et ouvrir des fichiers ADF.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Qu'est-ce qu'un fichier ADF ?

Un fichier avec l'extension .adf est un format de fichier de données raster utilisé par les applications logicielles ESRI telles qu'ArcGIS, ArcView et ArcInfo. Les données spatiales sont stockées sous la forme d'une grille binaire native d'ESRI. La grille est composée de lignes et de colonnes de cellules qui peuvent être entières ou à virgule flottante. Les grilles d'entiers dans un fichier ADF représentent des données discrètes et les grilles à virgule flottante représentent des données continues. Un autre format de fichier ESRI populaire est le fichier [SHP](/fr/gis/shp/) qui représente des informations géospatiales sous la forme de données vectorielles à utiliser par les applications de systèmes d'information géographique (SIG).

## Format de fichier ADF - Plus d'informations

Les fichiers ADF sont enregistrés sous forme de fichiers binaires sur disque dans une grille binaire. Les grilles d'entiers ont des attributs qui sont stockés dans une table d'attributs de valeur (VAT). Chaque valeur unique dans la grille a un enregistrement dans VAT où l'enregistrement stocke la valeur unique et le nombre de cellules dans la grille est représenté par cette valeur.

Les grilles à virgule flottante n'ont pas de TVA.

### Structure de la grille

Dans le fichier ADF, les grilles sont implémentées à l'aide d'une structure de données raster tuilée. L'unité de base à l'intérieur de cette structure de données raster est un bloc rectangulaire de cellules. Chaque bloc est stocké sur disque et compressé dans une structure de fichier de longueur variable, appelée tuile. Chaque bloc est stocké sous la forme d'un enregistrement de longueur variable.

Les rasters GRID sont stockés dans des espaces de travail, où un espace de travail contient un sous-répertoire d'informations et un sous-répertoire pour chaque GRID. Il existe plusieurs fichiers qui géolocalisent et attribuent des données pour la grille correspondante. Le sous-répertoire Info contient plusieurs fichiers qui conservent certaines informations sur le GRID et d'autres ensembles de données, tels que les couvertures, dans l'espace de travail.

## Références ##

* [Format de grille ESRI](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)


