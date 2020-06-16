{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "GML",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2019-09-10"
}

# What is a GML file? #

GML stands for Geography Markup Language that is based on XML specifications developed by the Open Geospatial Consortium (OGC). The format is used to store geographic data features for interchange among different file formats. It serves as a modeling language for geographic systems as well as an open interchange format for geographic transactions on the internet.

## GML File Format ##

As with most XML based grammars, there are two parts to the grammar – the schema that describes the document and the instance document that contains the actual data. A GML document is described using a GML Schema. This allows users and developers to describe generic geographic data sets that contain points, lines and polygons. Using application schemas, users can refer to roads, highways, and bridges instead of points, lines and polygons.

It is worth noticing that GML should not be interpreted for representation of spatial data on maps. The representation of GML content is different than the purpose for which GML was created. In short, GML is similar to XML in that it is only used for holding the spatial contents that can be used by mapping applications for display purpose.

### Content Formation in GML ###

GML represents spatial data using features which is a list of properties and geometries. A Property has a name, type and value description. Geometries are composed of basic geometry building blocks such as:

* points
* lines
* curves
* sufraces and 
* polygons

The future versions of GML are planned to support 3D geometry as well as topological relationships between features.

GML encoding already allows for quite complex features.  A feature can for example be composed of other features.  A single feature like an airport might thus be composed of other features such as taxi ways, runways, hangers and air terminals.  The geometry of a geographic feature can also be composed of many geometry elements.  A geometrically complex feature can thus consist of a mix of geometry types including points, line strings and polygons.

### Examples ###

GML 1.0 and 2.0 encode Polygons, Points and LineString objects as follow:

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

## References ##

* [GML Specifications](http://www.opengeospatial.org/standards/gml)
* [GML - By Wikipedia](https://en.wikipedia.org/wiki/Geography_Markup_Language)