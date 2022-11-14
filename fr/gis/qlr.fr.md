{
  "date" : "2019-10-11",
  "keywords" :[ "fichier qlr", "format de fichier qlr", "qu'est-ce qu'un fichier qlr", "fichier", "exemple qlr", "extension de fichier qlr","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - Fichier de définition de couche QGIS",
  "description":"En savoir plus sur le format de fichier QLR et les API qui peuvent créer et ouvrir des fichiers QLR.",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Qu'est-ce qu'un fichier QLR ?

Un fichier avec .qlr est un fichier de définition de couche qui contient un pointeur vers la source de données de la couche. Ceci s'ajoute aux informations de style [QGIS](https://www.qgis.org/en/site/) pour la couche. Ayant des références à tous les styles associés, ce fichier est utilisé comme une source unique de données à utiliser pour obtenir les informations de style. À l'aide des fichiers QLR, les informations sur les sources de données peuvent être placées dans ce fichier unique qui peut être lu par d'autres applications pour charger les informations de style. Les fichiers QLR peuvent être ouverts avec n'importe quel éditeur de texte tel que Notepad++.

## Format de fichier QLR

QLR, similaire à [QGS](/fr/gis/qgs/), est un fichier XML qui contient des pointeurs vers la source de données de la couche sous la forme de balises XML. Il est similaire au fichier ArcGIS .lyr. Les balises de niveau supérieur d'un fichier QML sont comme indiqué dans l'image ci-dessous.

{{< figure src="../qlr.png" title="" >}}

## Références

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

