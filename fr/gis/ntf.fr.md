{
  "date" : "2021-07-28",
  "keywords" :[ "fichier ntf", "format de fichier ntf", "qu'est-ce qu'un fichier ntf", "fichier", "exemple ntf", "extension de fichier ntf","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - Fichiers de format de transfert national",
  "description":"En savoir plus sur le format de fichier NTF et les API qui peuvent créer et ouvrir des fichiers NTF.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## Qu'est-ce qu'un fichier NTF ?
Les fichiers avec l'extension .ntf sont appelés les fichiers **National Transfer Format (NTF)** ; principalement utilisé par le UK Ordnance Survey (OS); spécifiquement pour le transfert de données géospatiales. Il est géré par la British Standards Institution. Il est devenu le format de transfert standard pour les données numériques de l'Ordnance Survey. La projection National Grid du Royaume-Uni, qui est un type de Transverse Mercator, contient toutes les informations géoréférencées pour les fichiers NTF.

## Format de fichier NTF
Le format de fichier NTF appartient à Ordnance Survey au Royaume-Uni ; pris en charge par la bibliothèque GDB pour l'importation. La version actuelle du format de fichier NTF est 2.0. Ce format de fichier a été introduit pour résoudre une limitation du segment vectoriel **PCIDSK** qui n'a qu'un seul champ d'attribut par structure, mais il existe une variété d'attributs qui peuvent être extraits avec des données vectorielles. Pour contourner le format de fichier NTF est constitué comme ayant deux segments. Chaque segment est constitué des mêmes vecteurs, mais avec des attributs différents. Le premier segment d'un fichier vectoriel NTF contient les vecteurs avec le numéro de code de caractéristiques comme attribut. Le deuxième segment contient les vecteurs avec la valeur comme attribut.

### Système de référencement de coordonnées
La bibliothèque GDB représente les données raster et vectorielles avec les caractéristiques de projection TM appropriées :

- Longitude de référence : 49,0
- Latitude de référence : 2.0
- Abscisse fausse : 400000
- Ordonnée fausse : -100000
- Échelle : 0,9996012717
- Ellipsoïde : Airy 1830 (E009)
Aucun support n'est disponible pour la mise à jour ou l'écriture de fichiers NTF, et les fichiers DTM ne peuvent pas non plus être liés.

### Exemple d'Ogrinfo
L'exemple suivant utilise **ogrinfo** sur un fichier NTF pour récupérer les numéros de couche :
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Références

* [Format de transfert national britannique (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Web Mapping - Illustrated by Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

