{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "Base de données SQLite du projet QGIS", "extension", "format", "QGIS", "Base de données auxiliaire", "Qu'est-ce qu'un fichier QGD"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - Base de données SQLite du projet QGIS",
  "description":"Découvrez QGD qui est une base de données sqlite du projet QGIS et des API qui peuvent créer et ouvrir des fichiers QGD.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Qu'est-ce qu'un fichier QGD ?

Le fichier avec l'extension .QGD est en fait la base de données sqlite associée du projet **QGIS** qui contient les données auxiliaires du projet. Le fichier QGD restera vide s'il n'y a pas de données auxiliaires pour le projet.

## Détails sur le format de fichier QGD

En mode classique, la base de données auxiliaire est enregistrée sous forme de fichier avec l'extension .qgd avec le fichier xml. Le système **Base de données auxiliaire** permet de lire et d'écrire des données dans le système de manière alternative. Lors de la création du QGZ qui est un conteneur compressé, le fichier .qgd est inclus dans le .qgz.

## Qu'est-ce qu'une base de données auxiliaire ?
La base de données auxiliaire est en fait un système de base de données de secours créé en réponse à la duplication de la base de données cible. La base de données auxiliaire est en fait un cas de base de données en double qui serait la base de données vers laquelle vous dupliquez. Par exemple, si vous configurez une base de données de secours à l'aide d'une base de données dupliquée, la base de données source sera la cible et la base de données de secours sera appelée auxiliaire.


## Références

* [QGZ - Un nouveau format de fichier de projet par défaut pour QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Formats de fichier QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

