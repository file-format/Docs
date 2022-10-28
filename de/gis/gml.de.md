{
  "date" : "2019-10-11",
  "keywords" :[ "gml-Datei", "was ist eine gml-Datei", "Datei", "gml-Beispiel", "gml-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML - Geographie-Markup-Language-Dateiformat",
  "description":"Erfahren Sie mehr über das GML-Dateiformat und APIs, die GML-Dateien erstellen und öffnen können.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine GML-Datei?

GML steht für Geography Markup Language, die auf XML-Spezifikationen basiert, die vom Open Geospatial Consortium (OGC) entwickelt wurden. Das Format wird verwendet, um geografische Datenmerkmale für den Austausch zwischen verschiedenen Dateiformaten zu speichern. Es dient als Modellierungssprache für geografische Systeme sowie als offenes Austauschformat für geografische Transaktionen im Internet.

## GML-Dateiformat ##

Wie bei den meisten XML-basierten Grammatiken besteht die Grammatik aus zwei Teilen – dem Schema, das das Dokument beschreibt, und dem Instanzdokument, das die eigentlichen Daten enthält. Ein GML-Dokument wird mithilfe eines GML-Schemas beschrieben. Dadurch können Benutzer und Entwickler generische geografische Datensätze beschreiben, die Punkte, Linien und Polygone enthalten. Mithilfe von Anwendungsschemata können Benutzer auf Straßen, Autobahnen und Brücken statt auf Punkte, Linien und Polygone verweisen.

Es ist erwähnenswert, dass GML nicht für die Darstellung von räumlichen Daten auf Karten interpretiert werden sollte. Die Darstellung von GML-Inhalten unterscheidet sich von dem Zweck, für den GML erstellt wurde. Kurz gesagt, GML ähnelt XML dahingehend, dass es nur zum Speichern der räumlichen Inhalte verwendet wird, die von Kartierungsanwendungen zu Anzeigezwecken verwendet werden können.

### Inhaltsbildung in GML ###

GML stellt räumliche Daten mithilfe von Merkmalen dar, bei denen es sich um eine Liste von Eigenschaften und Geometrien handelt. Eine Eigenschaft hat einen Namen, einen Typ und eine Wertbeschreibung. Geometrien bestehen aus grundlegenden Geometriebausteinen wie:

* Punkte
* Linien
* Kurven
* Flächen u
* Polygone

Die zukünftigen Versionen von GML sollen 3D-Geometrie sowie topologische Beziehungen zwischen Merkmalen unterstützen.

Die GML-Codierung ermöglicht bereits recht komplexe Funktionen. Ein Merkmal kann beispielsweise aus anderen Merkmalen zusammengesetzt sein. Ein einzelnes Merkmal wie ein Flughafen kann somit aus anderen Merkmalen wie Rollwegen, Start- und Landebahnen, Hangars und Luftterminals zusammengesetzt sein. Die Geometrie eines geografischen Features kann auch aus vielen Geometrieelementen bestehen. Ein geometrisch komplexes Merkmal kann somit aus einer Mischung von Geometrietypen bestehen, einschließlich Punkten, Linienzügen und Polygonen.

### Beispiele ###

GML 1.0 und 2.0 kodieren Polygone, Punkte und LineString-Objekte wie folgt:

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

## Verweise ##

* [GML-Spezifikationen](http://www.opengeospatial.org/standards/gml)
* [GML – Von Wikipedia](https://en.wikipedia.org/wiki/Geography_Markup_Language)

