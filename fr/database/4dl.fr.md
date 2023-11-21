{
  "date" : "2023-06-14",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Découvrez le format de fichier 4DL et les API permettant de créer et d'ouvrir des fichiers 4DL.",
  "title" :"4DL - Fichier journal de la base de données 4ème Dimension",
  "linktitle" : "4DL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-06-14"
}

## Qu'est-ce qu'un fichier 4DL ?

Un fichier journal 4DL permet d'enregistrer les modifications apportées à un fichier de base de données 4D (.4DD). Ce fichier est stocké avec le fichier de base de données et partage un nom de fichier similaire. Son objectif est de suivre avec précision et de conserver un enregistrement complet des mises à jour mises en œuvre dans la base de données. Un [fichier 4DD](/fr/database/4dd/), par rapport au fichier 4DL, est principalement associé à la 4ème Dimensions par 4D Inc.

## Format de fichier 4DL - Plus d'informations

En règle générale, plusieurs fichiers 4DL sont stockés avec un fichier 4DD. Ainsi, la première version du fichier journal peut être nommée 0001.4dl, mais les versions latérales des fichiers journaux seront enregistrées sous 0002.4dl, 0003.4dl, etc. Désormais, si le fichier journal lui-même subit 3 sauvegardes ultérieures, il sera étiqueté « db1[0005-0003].4dl ».

## Les références

* [4DD - Wikipedia](https://en.m.wikipedia.org/wiki/4th_Dimension_(software))
