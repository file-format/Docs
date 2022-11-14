{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - Fichier NGS SP3",
  "description":"En savoir plus sur le format de fichier SP3 et les API qui peuvent créer et ouvrir des fichiers SP3.",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Qu'est-ce qu'un fichier SP3 ?

Un fichier avec l'extension .sp3 est un format orbital National Geodetic Survey (NGS) pour stocker des informations orbitales. Il s'agit d'une extension des formats SP1 et SP2 de NGS, et inclut les informations de correction d'horloge satellite qui sont calculées simultanément avec les orbites. Il est principalement basé sur la position et l'horloge, et n'inclut pas les vitesses. Le format a été proposé dans Remondi, 1989 et a été adopté en 1991. En plus des informations de correction d'horloge satellite, il comprend des informations telles que les exposants de précision d'orbite, les lignes de commentaire, la semaine GPS et les secondes de la semaine associées à la première époque. Les fichiers SP3 peuvent être ouverts avec Wolfram Research Mathematica.

## Format de fichier SP3 - Plus d'informations

Les fichiers SP3 sont enregistrés sur le disque au format de fichier ASCII et son contenu peut être ouvert dans n'importe quel éditeur de texte pour être visualisé. La structure d'un fichier SP3 peut être vue dans l'image suivante.

{{< figure src="../sp3-file-format.png" title="" >}}

## Références

* [Le format d'orbite du produit standard étendu 3 (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,une structure%20plus%20flexible%20d'en-tête%20)
* [Extending the National Geodetic Survey Standard GPS Orbit Formats] (https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

