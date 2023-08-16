{
  "date" : "2021-07-29",
  "keywords" :[ "fichier gpkg", "format de fichier gpkg", "qu'est-ce qu'un fichier gpkg", "fichier", "exemple gpkg", "extension de fichier gpkg","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - Fichiers au format GeoPackage",
  "description":"En savoir plus sur le format de fichier GPKG et les API qui peuvent créer et ouvrir des fichiers GPKG.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Qu'est-ce qu'un fichier GPKG ?
Un fichier avec une extension .gpkg consiste en un système d'information géographique implémenté en tant que conteneur de base de données SQLite contenant des tables de données et de métadonnées avec des définitions typiques, des limitations de format, des assertions d'intégrité et des contraintes de contenu. Il a été publié en 2014; défini par l'OGC (Open Geospatial Consortium) pour le compte de l'armée américaine. Divers gouvernements, organisations commerciales et open source soutiennent largement le GeoPackage.

## Format de fichier GPKG
Un GeoPackage est constitué d'un fichier de base de données SQLite 3 étendu ; une norme définit un ensemble de règles (conventions requises) pour :
- Stockage d'ensembles d'images de matrice de tuiles
- Caractéristiques vectorielles
- Cartes raster à différentes échelles
- Métadonnées et schéma

Vous pouvez étendre un GeoPackage en utilisant les règles d'extension telles que définies dans la clause 2.3 de la norme. Le but de la conception d'un GeoPackage était de rendre une base de données aussi légère que possible et de l'inclure dans un fichier unique prêt à l'emploi. Cela le rend idéal pour les applications mobiles en mode hors ligne et le partage rapide sur le stockage en nuage ou les périphériques de stockage USB, etc.

### Contenu du GPKG
Les GeoPackages contiennent un certain nombre de tables, comme d'autres bases de données relationnelles. Ces tables peuvent être des tables définies par l'utilisateur ou des métadonnées. Les GeoPackages se composent de deux tables de métadonnées obligatoires :

#### gpkg_contents
Une table des matières pour un GeoPackage. Les colonnes obligatoires de ce tableau sont :

- **table_name** : le nom réel de la table de données définie par l'utilisateur ;
- **data_type** : le type de données, par exemple les titres, les caractéristiques et les attributs ;
- **identifiant et description** : texte lisible par l'homme ;
- **last_change** : la date informative du dernier changement, au format ISO 8601 ;
- **min_x, min_y, max_x et max_y** : les étendues spatiales du contenu. ;
- **srs_id** : système de référence spatiale .

#### gpkg_spatial_ref_sys
Pour le contenu de référence spatiale ; y compris, mais sans s'y limiter, les tuiles et les entités, chaque ligne du contenu doit faire référence à un système de référence de coordonnées ; stocké dans la table **gpkg_spatial_ref_sys**. Les colonnes obligatoires de ce tableau sont :

- **srs_name, description** : un nom et une description lisibles par l'homme pour le SRS ;
- **srs_id** : un identifiant unique pour le SRS ; également la clé primaire de la table ;
- **organisation** : nom insensible à la casse de l'organisation de définition.
- **organization_coordsys_id** : ID numérique du SRS attribué par l'organisation ;
- **définition** : définition du texte bien connu du SRS.


## Références

* [GeoPackage - par Wikipédia](https://en.wikipedia.org/wiki/GeoPackage)
* [Démarrer avec GeoPackage](http://www.geopackage.org/guidance/getting-started.html)

