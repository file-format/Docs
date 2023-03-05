{
  "date" : "2019-10-11",
  "keywords" :[ "fichier gml", "qu'est-ce qu'un fichier gml", "fichier", "exemple gml", "extension de fichier gml","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML - Format de fichier de langage de balisage géographique",
  "description":"En savoir plus sur le format de fichier GML et les API qui peuvent créer et ouvrir des fichiers GML.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier GML ?

GML signifie Geography Markup Language qui est basé sur les spécifications XML développées par l'Open Geospatial Consortium (OGC). Le format est utilisé pour stocker des caractéristiques de données géographiques pour l'échange entre différents formats de fichiers. Il sert de langage de modélisation pour les systèmes géographiques ainsi que de format d'échange ouvert pour les transactions géographiques sur Internet.

## Format de fichier GML ##

Comme avec la plupart des grammaires basées sur XML, la grammaire comporte deux parties : le schéma qui décrit le document et le document d'instance qui contient les données réelles. Un document GML est décrit à l'aide d'un schéma GML. Cela permet aux utilisateurs et aux développeurs de décrire des ensembles de données géographiques génériques contenant des points, des lignes et des polygones. À l'aide de schémas d'application, les utilisateurs peuvent faire référence à des routes, des autoroutes et des ponts au lieu de points, de lignes et de polygones.

Il convient de noter que GML ne doit pas être interprété pour la représentation de données spatiales sur des cartes. La représentation du contenu GML est différente de l'objectif pour lequel GML a été créé. En bref, GML est similaire à XML en ce sens qu'il n'est utilisé que pour contenir le contenu spatial qui peut être utilisé par les applications de cartographie à des fins d'affichage.

### Formation de contenu en GML ###

GML représente des données spatiales à l'aide d'entités qui sont une liste de propriétés et de géométries. Une propriété a un nom, un type et une description de valeur. Les géométries sont composées de blocs de construction géométriques de base tels que :

* points
* lignes
* courbes
* surfaces et
* polygones

Les futures versions de GML sont prévues pour prendre en charge la géométrie 3D ainsi que les relations topologiques entre les entités.

L'encodage GML permet déjà des fonctionnalités assez complexes. Une fonctionnalité peut par exemple être composée d'autres fonctionnalités. Une seule entité telle qu'un aéroport peut donc être composée d'autres entités telles que des voies de circulation, des pistes, des hangars et des aérogares. La géométrie d'une entité géographique peut également être composée de nombreux éléments géométriques. Une entité géométriquement complexe peut donc consister en un mélange de types de géométrie, notamment des points, des lignes brisées et des polygones.

### Exemples ###

GML 1.0 et 2.0 encodent les objets Polygones, Points et LineString comme suit :

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## Références ##

* [Spécifications GML](http://www.opengeospatial.org/standards/gml)
* [GML - Par Wikipédia](https://en.wikipedia.org/wiki/Geography_Markup_Language)

