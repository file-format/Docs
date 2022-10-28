{
  "date" : "2019-10-11",
  "keywords" :[ "shp-Datei", "shp-Dateiformat", "was ist eine shp-Datei", "Datei", "shp-Beispiel", "shp-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - ESRI Shapefile",
  "description":"Erfahren Sie mehr über das SHP-Dateiformat und APIs, die SHP-Dateien erstellen und öffnen können.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine SHP-Datei?

SHP ist die Dateierweiterung für einen der primären Dateitypen, der zur Darstellung von ESRI Shapefile verwendet wird. Es stellt Geoinformationen in Form von Vektordaten dar, die von Anwendungen von Geografischen Informationssystemen (GIS) verwendet werden. Das Format wurde als offene Spezifikation entwickelt, um die Interoperabilität zwischen ESRI und anderen Softwareprodukten zu erleichtern.

## Daten Präsentation

Wie bereits erwähnt, beschreibt ein Shapefile-Format Geoinformationen eines Datensatzes als Vektormerkmale. Zu diesen Vektormerkmalen gehören:

* Punkte
* Linien
* Polygone

Diese Features in Kombination können fast jede Art von Formen wie Wasserbrunnen, Landesgrenzen, räumliche Punkte, Flüsse, Seen usw. darstellen. Jedes Vektor-Feature kann Attribute haben, die den eigentlichen Zweck dieses Features definieren. Beispielsweise kann ein Shapefile, das die Städte Los Angeles enthält, den Namen der Stadt und die Temperatur als Attribute haben, was den räumlichen Daten eine aussagekräftige Darstellung verleiht.

## Zugehörige Dateien

Eine eigenständige shp-Datei kann von Softwareanwendungen nicht verwendet werden, um den darin enthaltenen Daten Bedeutung zu verleihen. Um die in einer solchen Datei enthaltenen Informationen zu verstehen, verwendet ein Shapefile die folgenden zusätzlichen obligatorischen Dateien.

* shx-Datei - Indexdatei
* dbf-Datei - eine dBASE-Datei, die alle Attribute der Formen in der Hauptdatei speichert
* prj-Datei - speichert Projektinformationen der Datei

Es kann auch andere optionale Dateien geben, die den gleichen Namen wie die Hauptdatei haben.

## SHP-Dateiformatspezifikationen

Offene Spezifikationen von Shapefiles sind online von ESRI in Form von [Technical Description] (http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) verfügbar und erläutern die Gesamtstruktur der Datei im Detail. Die Informationen in der .shp-Hauptdatei bestehen aus Headern und Datensätzen. Dem Dateiheader mit fester Länge folgen Datensätze mit variabler Länge, wobei jeder Datensatz aus einem Datensatzheader mit fester Länge besteht, gefolgt von Datensatzinhalten mit variabler Länge.

### Header der Haupt-SHP-Datei

Der Hauptdatei-Header beginnt am Anfang der Datei und ist 100 Byte lang. Die Organisation dieses Hauptdatei-Headers zusammen mit Byte-Position, Wert, Typ und Byte-Reihenfolge ist wie in der folgenden Tabelle gezeigt.


|Bytes|Feld|Wert|Typ|Byte-Reihenfolge
---|---|---|---|---|
|0-3|Dateicode|9994|Ganzzahl|Big Endian
|4-23|Nicht verwendet|0|Integer|Big Endian
|24-27|Dateilänge|Dateilänge|Integer|Big Endian
|28-31|Version|1000|Integer|Little Endian
|32-35|Formtyp|Formtyp|Integer|Little Endian
|36-67|Mindestbegrenzungsrechteck|Xmin, Ymin, Xmax und Ymax|double|Little Endian
|68-83|Bounding Box|Zmin, Zmax|doppelt|Little Endian
|84-99|Begrenzungsrahmen|Mmin, Mmax|doppelt|

Es sei darauf hingewiesen, dass der Wert der Dateilänge die Gesamtlänge der Datei in 16-Bit-Wörtern ist, die auch die fünfzig 16-Bit-Wörter umfasst, die den Header bilden.

#### Formtypen

Die Werte des Formtypfeldes in der obigen Tabelle lauten wie folgt:


|Wert|Formtyp
---|---|
|0|Nullform
|1|Punkt
|3|Polylinie
|5|Polygon
|8|Mehrpunkt
|11|PunktZ
|13|PolylinieZ
|15|PolygonZ
|18|MultiPointZ
|21|PunktM
|23|PolylinieM
|25|PolygonM
|28|MultiPointM
|31|MultiPatch

### Datensätze ###

Dem Hauptdateiheader folgen Datensätze mit variabler Länge, wobei jeder Datensatz aus einem Datensatzheader mit fester Länge besteht, gefolgt von Datensatzinhalten mit variabler Länge.

#### Kopfzeile des Datensatzes ####

Der Satzkopf enthält Informationen über Satznummer und Inhaltslänge des Satzes in einer festen Länge von 8 Byte. Die Organisation des Datensatzkopfes ist wie folgt:


|Bytes|Feld|Wert|Typ|Byte-Reihenfolge
---|---|---|---|---|
|0-3|Datensatznummer|Datensatznummer|Integer|Groß
|4-7|Aufzeichnungslänge|Aufzeichnungslänge|Integer|Groß

#### Inhalt des Datensatzes ####

Der Inhalt eines Shapefile-Datensatzes besteht aus einem Formtyp, gefolgt von den geometrischen Daten für diese Form. Ein Formtyp von 0 stellt eine Nullform dar, die keine geometrischen Daten für die Form hat. Die Länge des Datensatzinhalts spiegelt die Formteile und Eckpunkte wider. Nehmen wir ein Beispiel für den Typ Punktform, um zu erläutern, wie ein Datensatz Informationen über einen solchen Formtyp enthält.

Ein Punkt stellt einen bestimmten geografischen Ort in der Reihenfolge X,Y dar, wobei jede Koordinate durch einen Wert mit doppelter Genauigkeit dargestellt wird. Die folgende Tabelle zeigt die Anordnung eines Formtyps Punkt.


|Bytes|Formtyp|Wert|Typ|Zahl|Byte-Reihenfolge
---|---|---|---|---|---|
|0-3|Formtyp|1|Ganzzahl|1|Klein
|4-11|X|X|doppelt|1|Klein
|12-19|Y|Y|double|1|Klein

Beispiele für andere Formtypen finden Sie im technischen Beschreibungsdokument von ESRI.

## Verweise ##

* [ESRI Shapefile Technical Description](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) von ESRI

