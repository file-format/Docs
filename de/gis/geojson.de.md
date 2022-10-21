{
  "date" : "2019-10-11",
  "keywords" :[ "geojson-Datei", "was ist eine geojson-Datei", "Datei", "geojson-Beispiel", "geojson-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - JSON-basiertes geografisches Dateiformat",
  "description":"Erfahren Sie mehr über das GeoJSON-Dateiformat und APIs, die GeoJSON-Dateien erstellen und öffnen können.",
  "linktitle" :"GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine GeoJSON-Datei?

GeoJSON ist ein JSON-basiertes Format, das entwickelt wurde, um die geografischen Merkmale mit ihren nicht räumlichen Attributen darzustellen. Dieses Format definiert verschiedene JSON-Objekte (JavaScript Object Notation) und ihre Verknüpfungsart. Das JSON-Format stellt kollektive Informationen über die geografischen Merkmale, ihre räumlichen Ausdehnungen und Eigenschaften dar. Ein Objekt dieser Datei kann eine Geometrie (Point, LineString, Polygon), ein Feature oder eine Sammlung von Features anzeigen. Die Features geben Adressen und Orte als Straßen von Punkten, Hauptstraßen und Grenzen als Linienzüge und Länder, Provinzen und Landregionen als Polygone wieder. Mithilfe von GeoJSON können verschiedene mobile Routing- und Navigationsanwendungen die Abdeckung ihrer Dienste angeben. Eine Erweiterung von GeoJSON ist TopoJSON, das kleiner ist und die räumliche Topologie codiert.

## Kurze Geschichte ##

Die Internet Engineering Task Force (IETF) hat in Zusammenarbeit mit den Autoren des Formats eine [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) gebildet, um GeoJSON im April 2015 zu veröffentlichen. Es ersetzt 2008 GeoJSON-Spezifikation, [RFC 7946](https://tools.ietf.org/html/rfc7946), die neue Standardspezifikation des GeoJSON-Formats, veröffentlicht im August 2016.

## GeoJSON-Dateiformat ##

### Koordinate ###

Koordinaten sind das Grundelement aller geografischen Daten. Dies ist eine einzelne Dimension (Längengrad, Breitengrad), die eine einzelne Zahl (Dezimalformat) darstellt und manchmal auch eine Koordinate für die Höhe aufzeichnet. Zeit ist auch eine Dimension, aber ihre Komplexität macht es schwierig, sie als Koordinate aufzuzeichnen. Koordinaten in beiden JSON GeoJSON sind wie Zahlen formatiert.

### Position ###

Ein geordnetes Array von Koordinaten repräsentiert die [Position](http://geojson.org/geojson-spec.html#positions). Dies ist die kleinste Einheit, die einen Punkt auf der Erde anzeigen kann.

`[Längengrad, Breitengrad, Höhe]`

Vor der Veröffentlichung der aktuellen Spezifikation erlaubte GeoJSON die Aufzeichnung von drei Koordinaten pro Position, dies ist jedoch nach der neuen Spezifikation nicht zulässig.

### Geometrie ###

Geometrien sind einfache Formen (Punkte, Kurven und Oberflächen) in GeoJSON, die aus einem Typ und einer Sammlung von Koordinaten bestehen. Punkt ist die einfachste Geometrie, die eine einzelne Position darstellt

`{ "Typ": "Punkt", "Koordinaten": [0, 0] }`

### Zeilenfolgen ###

Mindestens zwei verbundene Orte werden verwendet, um eine Linie darzustellen.

`{ "type": "LineString", "coordinates": [[10, 30], [10, 10]] }`

Punkt- und Linienzüge sind die zwei einfachsten Kategorien der Geometrie. Beide Arten von Geometrie stören viele geometrische Regeln nicht. Ein Punkt kann an einer beliebigen Stelle dargestellt werden, und eine Linie kann mehr als einen Punkt haben, selbst wenn sich die Punkte selbst kreuzen.

### Polygone ###

GeoJSON-Geometrien scheinen in Polygonen deutlich komplexer zu sein. Polygone haben Innen- und Außenflächen und können darin Löcher aufweisen.

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

Im Vergleich zu LineStrings ist die Koordinatenliste in Polygonen eine weitere Ebene verschachtelt und kann Ausschnitte wie Donuts haben.

### Koordinatenebene ###

Im GeoJSON-Format gibt es für die Eigenschaft „Koordinaten“ vier Tiefenebenen.

### Merkmale ###

Geometrien sind der zentrale Bestandteil von GeoJSON, daher sind die Daten der realen Welt mehr als diese einfachen Formen mit Identität und Attributen. Features erfassen die Geometrie sowie deren Eigenschaften.

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

Eine Feature-Eigenschaft kann eine Art [JSON](http://json.org/)-Objekt sein, das Schlüsselwertzuordnungen mit einfacher Tiefe enthält.

### FeatureCollection ###

Auf der obersten Ebene von GeoJSON-Dateien ist FeatureCollection die häufigste Sache, die so aussieht:

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

Viele Mapping- und GIS-Softwarepakete unterstützen GeoJSON, einschließlich GeoDjango, OpenLayers und Geoforge-Software. Es ist auch mit PostGIS und Mapnik kompatibel. Auch die API-Dienste von Google, Yahoo und Bing Maps unterstützen GeoJSON.

## Verweise ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON – Von Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)

