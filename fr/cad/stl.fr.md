{
  "date" : "2020-03-16",
  "keywords" :[ "Fichier STL", "Format", "CAO" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier STL et les API qui peuvent créer et ouvrir des fichiers STL.",
  "title" :"Format de fichier STL",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier STL ?

STL, abréviation de stéréolithographie, est un format de fichier interchangeable qui représente la géométrie de surface en 3 dimensions. Le format de fichier trouve son utilisation dans plusieurs domaines tels que le prototypage rapide, l'impression 3D et la fabrication assistée par ordinateur. Il représente une surface comme une série de petits triangles, appelés facettes, où chaque facette est décrite par une direction perpendiculaire et trois points représentant les sommets du triangle. Les données résultantes sont utilisées par les applications pour déterminer la section transversale de la forme 3D à construire par le fabricant. Aucune information n'est disponible dans le format de fichier STL pour la représentation de la couleur, de la texture ou d'autres attributs de modèle [CAO](/fr/cad/) courants.

## Bref historique ##

Le développement du format de fichier STL remonte à 1987. Il a été développé par 3D Systems pour son utilisation dans les imprimantes 3D commerciales. Une version révisée du format de fichier STL, connue sous le nom de STL 2.0, a été proposée en 2009 avec des mises à jour du format de fichier.

## Spécifications du format de fichier ##

Un fichier STL représente une géométrie de surface à l'aide de facettes. Les facettes définissent la surface d'un objet 3D et sont identifiées de manière unique par une unité normale, qui est une ligne perpendiculaire au triangle de longueur 1,0, et par trois sommets. Il y a un total de 12 nombres stockés pour chaque facette en tant que normale et chaque sommet est spécifié par trois coordonnées chacun. Le fichier StL ne contient aucune information d'échelle ; les coordonnées sont en unités arbitraires.

Les spécifications du format de fichier STL peuvent être examinées sous deux aspects.

### Orientation des facettes ###

L'orientation d'une facette est déterminée par la direction de la normale unitaire et l'ordre dans lequel les sommets sont répertoriés. L'orientation des facettes est spécifiée de deux manières comme suit :

* La direction de la normale est vers l'extérieur
* Les sommets sont répertoriés dans le sens antihoraire depuis l'extérieur, en respectant la règle de la main droite.

### Règle sommet à sommet ###

Selon cette règle, chaque triangle partage deux sommets avec chacun de ses triangles adjacents. Ainsi, un sommet d'un triangle ne peut pas se trouver sur le côté d'un autre triangle.

## Format de fichier ##

STL est disponible en représentations ASCII et binaires pour un format de fichier compact.

### Format STL ASCII ###

La version ASCII du format de fichier STL est écrite en ASCII brut. Cependant, en raison de sa grande taille, le format de fichier n'est pas sélectionné comme format préférable pour l'utilisation. La syntaxe d'un fichier ASCII STL est la suivante :
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
Les mots en gras représentent des mots-clés qui doivent toujours être en minuscules. Les symboles en italique sont des variables qui doivent être remplacées par des valeurs spécifiées par l'utilisateur. Les données numériques dans les lignes **facette normale** et **sommet** sont des flottants simple précision, par exemple, 1,23456E+789. Une coordonnée **normale à la facette** peut avoir un signe moins au début ; une coordonnée **vertex** peut ne pas l'être.

### Format binaire STL ###

Le format binaire utilise l'entier IEEE et la représentation numérique à virgule flottante. Le format de fichier est représenté comme suit :

|Champ|Infos|
---|---|
|En-tête|80 caractères|
|Nombre de triangles|Entier petit endian non signé de 4 octets|
|Données pour chaque triangle|12 nombres à virgule flottante 32 bits|

Une vue plus élaborée du format de fichier est illustrée ci-dessous.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Références ##

* [Le format STL] (http://www.fabbers.com/tech/STL_Format)
* [STL - par Wikipédia](https://en.wikipedia.org/wiki/STL_(file_format))

