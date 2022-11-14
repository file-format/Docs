{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "fichier", "extension", "format", "format de fichier 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier PLY et les API qui peuvent créer et ouvrir des fichiers PLY.",
  "title" :"PLY - Format de fichier 3D polygone",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier PLY ?

PLY, Polygon File Format, représente un format de fichier 3D qui stocke des objets graphiques décrits comme une collection de polygones. Le but de ce format de fichier était d'établir un type de fichier simple et facile qui est suffisamment général pour être utile pour une large gamme de modèles. Le format de fichier PLY est disponible au format ASCII ainsi qu'au format binaire pour un stockage compact et pour une sauvegarde et un chargement rapides. Le format de fichier est utilisé par différentes applications qui prennent en charge la lecture de fichiers 3D.

Les objets au format PLY sont décrits par une collection de sommets, de faces et d'autres éléments, ainsi que des propriétés telles que la couleur et la direction normale qui peuvent être attachées à ces éléments. D'autres propriétés qui peuvent également être stockées avec l'objet incluent :

* Normales de surface
* coordonnées de texture
* transparence
* confiance des données de plage
* propriétés pour l'avant et l'arrière d'un polygone

Un objet représenté au format PLY peut être le résultat de diverses sources telles que des objets numérisés à la main, des objets polygonaux d'applications de modélisation, des données de distance, des triangles de cubes de marche, des données de terrain et des modèles de radiosité.

## Bref historique

Le format PLY a été développé dans les années 1990 par Greg Turk et d'autres dans le laboratoire graphique de Stanford et c'est pourquoi il est également connu sous le nom de Stanford Triangle Format. Le format de fichier a la version 1.0 depuis lors et aucune autre modification n'a été effectuée.

## Format de fichier PLY

Un objet PLY simple consiste en une collection d'éléments pour la représentation de l'objet. Il se compose d'une liste de triplets (x, y, z) d'un sommet et d'une liste de faces qui sont en fait des indices dans la liste des sommets. Les sommets et les faces sont deux exemples d'éléments et la majorité du fichier PLY se compose de ces deux éléments. De nouvelles propriétés peuvent également être créées et attachées aux éléments d'un objet, mais celles-ci doivent être ajoutées de manière à ce que les anciens programmes ne se cassent pas lorsque ces nouvelles propriétés sont rencontrées. De telles propriétés peuvent également être ignorées en lisant des applications. De plus, de nouveaux éléments peuvent être créés et des propriétés peuvent également être définies avec cet élément.

### Structure du fichier

La structure de fichier d'un format de fichier PLY est la suivante :

|Champ
---|
|En-tête de fichier
|Liste des sommets
|Liste des visages
|Liste des autres éléments

#### Structure d'exemple

Nous utiliserons l'exemple suivant ci-dessous dans notre discussion ultérieure pour différentes parties d'un format de fichier PLY.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### En-tête de fichier

L'en-tête du format de fichier PLY se compose de texte ASCII pour le format ASCII et binaire. Le début et la fin de la section d'en-tête sont identifiés par les mots-clés ply et end-header. Le début de l'en-tête contient le mot magique ply qui est utilisé pour la reconnaissance du format de fichier PLY par les lecteurs. La ligne suivante affiche le numéro de version de ce fichier. Les commentaires dans un format de fichier PLY commencent par le mot-clé de commentaire au début de chaque ligne de commentaire.

#### Mot-clé de l'élément

Le mot-clé element indique alors ce qu'il y a à l'intérieur du fichier. Elle est suivie de propriétés pour ce type d'élément spécifique où chaque propriété a son type de propriété et son ordre spécifiés comme indiqué ci-dessous :

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

Dans cet exemple particulier, l'élément de sommet spécifique a 3 propriétés de type float avec leur ordre spécifié.

#### Types de types de données

Il existe deux types de types de données qu'une propriété peut avoir.

`Scalar` : les types de données scalaires sont les suivants :

|#Nom|#Type|#Nombre d'octets
|car|caractère|1
|uchar|caractère non signé|1
|court|entier court|2
|ushort|entier court non signé|2
|int|Entier|4
|uint|Entier non signé|4
|float|flottant simple précision|4
|double|flottant double précision|8

`Liste` : il existe une forme spéciale de définitions de propriété qui utilise le type de données de liste. Un exemple de ceci provient du fichier de cube ci-dessus :

`liste de propriétés uchar int vertex_index`

Cela signifie que la propriété "vertex_index" contient d'abord un caractère non signé indiquant le nombre d'indices que contient la propriété, suivi d'une liste contenant autant d'entiers. Chaque entier de cette liste de longueur variable est un index vers un sommet.

## Références ##

* [Format de fichier PLY] (http://paulbourke.net/dataformats/ply/)
* [PLY - Par Wikipédia](https://en.wikipedia.org/wiki/PLY_(file_format))

