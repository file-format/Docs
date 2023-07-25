{
  "date" : "2019-10-11",
  "keywords" :[ "fichier geojson", "qu'est-ce qu'un fichier geojson", "fichier", "exemple geojson", "extension de fichier geojson","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - Format de fichier géographique basé sur JSON",
  "description":"En savoir plus sur le format de fichier GeoJSON et les API qui peuvent créer et ouvrir des fichiers GeoJSON.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier GeoJSON ?

GeoJSON est un format basé sur JSON conçu pour représenter les entités géographiques avec leurs attributs non spatiaux. Ce format définit différents objets JSON (JavaScript Object Notation) et leur mode de jonction. Le format JSON représente une information collective sur les entités géographiques, leurs étendues spatiales et leurs propriétés. Un objet de ce fichier peut indiquer une géométrie (Point, LineString, Polygon), une entité ou une collection d'entités. Les entités reflètent les adresses et les lieux sous forme de rues de point, les routes principales et les frontières sous forme de chaînes de lignes et les pays, provinces et régions terrestres sous forme de polygones. Grâce au GeoJSON, différentes applications mobiles de routage et de navigation peuvent indiquer la couverture de leurs services. Une extension de GeoJSON est TopoJSON qui est de plus petite taille et encode la topologie géospatiale.

## Bref historique ##

L'Internet Engineering Task Force (IETF), en association avec les auteurs du format, a formé un [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) pour publier GeoJSON en avril 2015. Remplacer le 2008 Spécification GeoJSON, [RFC 7946](https://tools.ietf.org/html/rfc7946), la nouvelle spécification standard du format GeoJSON publiée en août 2016.

## Format de fichier GeoJSON ##

### Coordonnées ###

Les coordonnées sont l'élément de base de toute donnée géographique. Il s'agit d'une seule dimension (longitude, latitude) représentant un seul nombre (format décimal) et enregistre parfois également une coordonnée pour l'élévation. Le temps est aussi une dimension mais sa complexité rend difficile son enregistrement en tant que coordonnée. Les coordonnées dans les deux JSON GeoJSON sont formatées comme des nombres.

### Position ###

Un tableau ordonné de coordonnées représente la [position](https://geojson.org/geojson-spec.html#positions). C'est la plus petite unité qui peut indiquer un point sur terre.

`[Longitude, latitude, élévation]`

Avant la publication de la spécification actuelle, GeoJSON permettait d'enregistrer trois coordonnées par position mais n'est pas autorisé par la nouvelle spécification.

### Géométrie ###

Les géométries sont des formes simples (points, courbes et surfaces) dans GeoJSON qui consistent en un type et une collection de coordonnées. Le point est la géométrie la plus simple qui représente une seule position

`{ "type": "Point", "coordonnées": [0, 0] }`

### Chaînes de lignes ###

Au moins deux places connectées sont utilisées pour représenter une ligne.

`{ "type": "LineString", "coordinates": [[10, 30], [10, 10]] }`

Les chaînes de points et de lignes sont les deux catégories de géométrie les plus simples. Les deux types de géométrie ne dérangent pas beaucoup de règles géométriques. Un point peut être représenté à un endroit n'importe où, et une ligne peut avoir plus d'un point, même si les points se croisent.

### Polygones ###

Les géométries GeoJSON semblent nettement plus complexes dans Polygons. Les polygones ont des zones intérieures et extérieures et peuvent avoir des trous à l'intérieur.

```
{
  "type": "Polygon",
  "Coordinates": [
    [
      [30, 10], [10, 10], [10, 0], [20, 40]
    ]
  ]
}
```

Par rapport aux LineStrings, dans les polygones, la liste des coordonnées est un niveau de plus imbriqué et peut avoir des découpes comme des beignets.

### Niveau de coordonnées ###

Au format GeoJSON, pour la propriété de coordonnées, il existe quatre niveaux de profondeur.

### Fonctionnalités ###

Les géométries sont la partie centrale de GeoJSON, par conséquent, les données du monde réel sont plus que ces simples formes ayant une identité et des attributs. Les fonctions enregistrent la géométrie ainsi que leurs propriétés.

```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [20, 10]
},
  "properties": {
    "name": "fortune island"
  }
}

```

Une propriété de fonctionnalité peut être un type d'objet [JSON](http://json.org/) contenant des mappages de valeur de clé à profondeur unique.

### FeatureCollection ###

Au niveau supérieur des fichiers GeoJSON, FeatureCollection est la chose la plus courante qui ressemble à :

```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [20, 10]
    },
      "properties": {
        "name": "null island"
  }
}
  ]
}
```

De nombreux progiciels de cartographie et SIG prennent en charge GeoJSON, notamment les logiciels GeoDjango, OpenLayers et Geoforge. Il est également compatible avec PostGIS et Mapnik. Les services API de Google, Yahoo et Bing Maps prennent également en charge GeoJSON.

## Références ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - Par Wikipédia](https://en.wikipedia.org/wiki/GeoJSON)

