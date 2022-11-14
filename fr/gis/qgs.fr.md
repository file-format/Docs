{
  "date" : "2019-10-11",
  "keywords" :[ "fichier qgs", "format de fichier qgs", "qu'est-ce qu'un fichier qgs", "fichier", "exemple qgs", "extension de fichier qgs","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - Format de fichier de projet QGIS",
  "description":"En savoir plus sur le format de fichier QGS et les API qui peuvent créer et ouvrir des fichiers QGS.",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier QGS ?

Un fichier avec l'extension .qgs est un fichier de projet créé avec [QGIS](https://www.qgis.org/en/site/), qui est une application SIG multiplateforme open source. Tous les paramètres du projet tels que les propriétés de la couche et les données auxiliaires du projet. Il est créé lorsqu'un projet cartographique est enregistré sur le disque. Il s'agit en fait d'un fichier de configuration qui conserve des informations telles que des pointeurs vers les données SIG, des informations de style sur les couches et le titre du projet. Les fichiers QGS peuvent être ouverts avec le logiciel QGIS téléchargeable gratuitement.

## Format de fichier QGS

Les fichiers QGS sont au format [XML](/fr/web/xml/) et stockent les données des projets sous forme de balises XML. Un fichier QGS contient des informations telles que :

* Titre du projet
* projet CRS
* l'arbre des couches
* paramètres d'accrochage
* relations
* l'étendue du canevas de la carte
* modèles de projet
* Légende
* docks mapview (2D et 3D)
* les calques avec des liens vers les ensembles de données sous-jacents (sources de données) et d'autres propriétés de calque, notamment l'étendue, le SRS, les jointures, les styles, le rendu, le mode de fusion, l'opacité, etc.
* propriétés du projet

### Balises XML de niveau supérieur QGS

{{< figure src="../qgstoplevel.png" title="" >}}

### Balises de couche de projet étendues de niveau supérieur

{{< figure src="../qgstoplevel.png" title="" >}}

## Références

* [QGIS](https://www.qgis.org/en/site/)

