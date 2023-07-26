{
  "date" : "2021-07-29",
  "keywords" :[ "fichier shx", "format de fichier shx", "qu'est-ce qu'un fichier shx", "fichier", "exemple shx", "extension de fichier shx","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - Format d'index de forme de fichier de formes",
  "description":"En savoir plus sur le format de fichier SHX et les API qui peuvent créer et ouvrir des fichiers SHX.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Qu'est-ce qu'un fichier SHX ?
Le fichier SHX appartient au format d'index de forme qui est un index de position de la géométrie de l'entité pour permettre une recherche rapide vers l'avant et vers l'arrière. Le SHX est un fichier offset à accès direct. Il n'y a pas de données dans ce fichier, seulement une copie en double des cent premiers octets, du numéro d'enregistrement et du décalage par rapport à l'octet de départ de cet enregistrement dans le shp. Veuillez noter que le fichier avec l'extension .shx ne lie pas le [SHP](/fr/gis/shp/) et [DBF](/fr/database/dbf/).

## Format de fichier SHX
Le format SHX contient un index de position de la géométrie de l'entité et un en-tête de 100 octets similaire au fichier SHP, suivi d'un nombre quelconque d'enregistrements de longueur fixe de 8 octets contenant les deux champs suivants :
| Octets | Taper | Endianité | Utilisation |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | grand | Décalage d'enregistrement (en mots de 16 bits) |
| 4–7 | int32 | grand | Longueur d'enregistrement (en mots de 16 bits) |

Cet index permet d'effectuer une recherche vers l'arrière dans le shapefile en, d'abord, en recherchant vers l'arrière dans l'index de forme puis en lisant l'offset d'enregistrement. Ce décalage peut être utilisé pour rechercher la position correcte dans le fichier SHP. Vous pouvez également chercher vers l'avant ; un nombre arbitraire d'enregistrements en utilisant la même méthode. Bien qu'il soit possible de générer un index complet avec un fichier SHP, cela peut augmenter les chances de corrompre rapidement le fichier SHP.


## Références

* [Shapefile - par Wikipédia)](https://en.wikipedia.org/wiki/Shapefile)


