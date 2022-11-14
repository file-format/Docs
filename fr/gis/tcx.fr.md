{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier TCX - Fichier XML du centre de formation",
  "description":"En savoir plus sur le format de fichier TCX et les API qui peuvent créer et ouvrir des fichiers TCX.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Qu'est-ce qu'un fichier TCX ?

Un fichier TCX (Training Center XML) est un format d'échange de données utilisé pour partager des données entre des appareils de fitness. Il a été introduit en 2008 avec le produit Training Center de Garmin. Les données d'entraînement telles que la fréquence cardiaque, la cadence de course, la cadence du vélo, les calories et le temps au tour sont stockées au format [XML](/fr/web/xml/) dans le fichier TCX. De plus, des données récapitulatives sur la piste d'entraînement sont également incluses dans le fichier TCX. Les fichiers TCX sont similaires aux fichiers [FIT](/fr/gis/fit/) créés avec les appareils portables de sport Garmin.

## Format de fichier TCX - Plus d'informations

Les fichiers TCX sont enregistrés sur le disque en tant que fichiers XML, chaque enregistrement étant enregistré en tant qu'activité. Une activité comprend toutes les données d'un entraînement telles que l'heure, le temps au tour, l'identifiant, la fréquence cardiaque, l'intensité, la cadence et les informations de piste qui contiennent les paires de position avec l'horodatage pour cette position lat-long semblable au [GPX] (/fr/gis/gpx/).

### Versions du format de fichier TCX

Il existe deux versions de ce format avec leurs propres schémas XML hébergés par Garmin. Voici quelques-uns d'entre eux:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## Protocole de données TCX

Une version rapide du format XML TCX est disponible sur Github en tant que [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Références ##

* [Centre de formation XML] (https://en.wikipedia.org/wiki/Training_Center_XML)
* [Visionneuse TCX](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

