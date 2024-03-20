{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier FMW - Format de fichier de l'atelier FME",
  "description":"En savoir plus sur le format de fichier FMW et les API qui peuvent créer et ouvrir des fichiers FMW.",
  "linktitle" : "FMW",
  "menu" : {
    "docs" : {
      "identifier":"gis-fmw",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Qu'est-ce qu'un fichier FMW ?

Un fichier FMW est un fichier de projet créé avec le logiciel FME Workbench (fait partie de la suite FME Desktop) qui est utilisé pour la transformation de données spatiales. Il contient des paramètres définis par l'utilisateur utilisés pour la manipulation de données spatiales, tels que des ensembles de données d'entrée, des propriétés de traduction, des projections et des paramètres de sortie. Les paramètres de manipulation des données spatiales sont stockés sous forme de mise en page visuelle et sont faciles à modifier et à enregistrer à nouveau.

Vous pouvez ouvrir les fichiers FMW à l'aide de [Safe Software FME Desktop](https://fme.safe.com/platform/).

## Format de fichier FMW - Plus d'informations

Les fichiers FMW sont stockés sur disque sous forme de fichiers binaires et peuvent être lus uniquement à l'aide du logiciel FME Desktop. Le logiciel peut également lire des données à partir d'un certain nombre de formats de bases de données relationnelles et prend également en charge une gamme de formats de données.

### Faits en bref FMW

|Fait|Valeur|
---|---|
|Lecteur/Ecrivain|Lecteur|
|Niveau de licence|Base|
|Dépendances|Aucune|
|Type de jeu de données|Fichier|
|Type de fonctionnalité|Fixé|
|Extensions de fichier typiques|.fmw|
|Support de traduction automatique|Oui|
|Attributs définis par l'utilisateur|Non|
|Prise en charge du système de coordonnées|Non|
|Prise en charge des couleurs génériques|Non|
|Index spatial|Non|
|Schéma requis|Non|
|Soutien aux transactions|Non|
|Attribut de type de géométrie|Aucun|
|Prise en charge de l'encodage|Non|

### Prise en charge de la géométrie FMW

|Géométrie|Supporté ?|
---|---|
|agrégé|non|
|cercles|non|
|arc de cercle|non|
|polygone en anneau|non|
|arc elliptique|non|
|points de suspension|non|
|ligne|non|
|aucun|oui|
|point|non|
|polygone|non|
|raster|non|
|solide|non|
|surface|non|
|texte|non|
|valeurs z|non|


## Références

* [Safe Software FME Desktop](https://fme.safe.com/platform/)
* [Faits en bref FMW](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_ReadersWriters/fmw/quick_facts_fmw.htm)
