{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "GeoJSON",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2019-09-10"
}

# What is a GeoJSON file? #

GeoJSON is a JSON based format designed to represent the geographical features with their non-spatial attributes. This format defines different JSON (JavaScript Object Notation) objects and their joining fashion. JSON format represents a collective information about the Geographical features, their spatial extents, and properties. An object of this file may indicate a geometry (Point, LineString, Polygon), a feature or collection of features. The features reflect addresses and places as point’s streets, main roads and borders as line strings and countries, provinces, and land regions as polygons. Using the GeoJSON, different mobile routing and navigation applications can indicate the coverage of their services. An extension of GeoJSON is TopoJSON that is smaller in size and encodes geospatial topology.

## Brief History ##

The Internet Engineering Task Force (IETF), in association with the format authors, shaped a [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) to release GeoJSON in April 2015. Replacing the 2008 GeoJSON specification, [RFC 7946](https://tools.ietf.org/html/rfc7946), the new standard specification of the GeoJSON format published in August 2016.

## GeoJSON File Format ##

### Coordinate ###

Coordinate** **is the basic element of any geographic data. This is a single dimension (Longitude, latitude) representing a single number (decimal format) and sometimes record a coordinate for elevation too. Time is a dimension too but its complexity makes it difficult to record it as coordinate. Coordinates in both JSON GeoJSON are formatted like numbers.

### Position ###

An ordered array of coordinates represent the [position](http://geojson.org/geojson-spec.html#positions).  This is the smallest unit that can indicate a point on earth.

//[Longitude, latitude, elevation]//

{{{Before the release of the current specification, GeoJSON allowed to record three coordinates per position but is not allowed by the new specification.}}}

### Geometry ###

Geometries are simple shapes (points, curves, and surfaces) in GeoJSON which consist of a type and a collection of coordinates. Point is the simplest geometry that** **represents a single position

//{ "type": "Point", "coordinates": [0, 0] }//

### LineStrings ###

At least two connected places are used to represent a line**.**

//{{{{ "type": "LineString", "coordinates": [[10, 30], [10, 10]] }}}}//

Point and line strings are the two simplest categories of geometry. Both types of geometry don’t bother many geometric rules. A point can be represented in a place anywhere, and a line can have more than one points, even if the points are self-crossing.

### Polygons ###

GeoJSON geometries seem significantly more complex in Polygons. Polygons have insides & outsides areas and can possess holes in that inside.

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

As compare to LineStrings, in polygons, the list of coordinate is one more level nested and can have cut-outs like donuts.

### Coordinate Level ###

In GeoJSON format, for the coordinate property, there are four ‘levels of depth’.

![](gis.geojson.WebHome@1556643359194-196.png)

### Features ###

Geometries are the central part of GeoJSON, therefore, the real world data is more than theses simple shapes having identity and attributes. Features records the geometry as well as their properties.

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

A feature properties can be a type of [JSON](http://json.org/) object contain single-depth key⇢ value mappings.

### FeatureCollection ###

At the top level of GeoJSON files, FeatureCollectionis the most common thing that  looks like: 

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

A lot of mapping and GIS software packages support GeoJSON including GeoDjango, OpenLayers, and Geoforge software. It is also compatible with PostGIS and Mapnik. The API services of Google, yahoo and Bing maps also support GeoJSON.

## References ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - By Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)