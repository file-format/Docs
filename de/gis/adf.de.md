{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - ESRI ArcInfo Binary Grid Format",
  "description":"Erfahren Sie mehr über das ADF-Dateiformat und APIs, die ADF-Dateien erstellen und öffnen können.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
"Bezeichner": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Was ist eine ADF-Datei?

Eine Datei mit der Erweiterung .adf ist ein Rasterdatendateiformat, das von ESRI-Softwareanwendungen wie ArcGIS, ArcView und ArcInfo verwendet wird. Räumliche Daten werden als ESRI-eigenes Binärgitter gespeichert. Das Raster besteht aus Zeilen und Spalten von Zellen, die sowohl Ganzzahlen als auch Gleitkommazahlen sein können. Ganzzahlgitter in einer ADF-Datei stellen diskrete Daten dar und Fließkommagitter stellen kontinuierliche Daten dar. Ein weiteres beliebtes ESRI-Dateiformat ist die [SHP](/de/gis/shp/)-Datei, die Geoinformationen in Form von Vektordaten darstellt, die von Geographic Information Systems (GIS)-Anwendungen verwendet werden.

## ADF-Dateiformat – Weitere Informationen

ADF-Dateien werden als Binärdateien in einem Binärraster auf der Disc gespeichert. Ganzzahlgitter haben Attribute, die in einer Wertattributtabelle (VAT) gespeichert sind. Jeder eindeutige Wert im Raster hat einen Datensatz in der Mehrwertsteuer, in dem der Datensatz den eindeutigen Wert speichert und die Anzahl der Zellen im Raster durch diesen Wert dargestellt wird.

Floating Point Grids haben keine Mehrwertsteuer.

### Gitterstruktur

Innerhalb der ADF-Datei werden Gitter mithilfe einer gekachelten Rasterdatenstruktur implementiert. Die Grundeinheit innerhalb dieser Rasterdatenstruktur ist ein rechteckiger Zellenblock. Jeder Block wird auf einer Disc gespeichert und in einer Dateistruktur mit variabler Länge komprimiert, die als Kachel bezeichnet wird. Jeder Block wird als ein Datensatz variabler Länge gespeichert.

GRID-Raster werden in Workspaces gespeichert, wobei ein Workspace ein info-Unterverzeichnis und ein Unterverzeichnis für jedes GRID enthält. Es gibt mehrere Dateien, die den geografischen Standort und Attributdaten für das entsprechende Raster enthalten. Das Unterverzeichnis „Info“ enthält mehrere Dateien, die bestimmte Informationen über das GRID und andere Datensätze, wie z. B. Coverages, im Arbeitsbereich enthalten.

## Verweise ##

* [ESRI-Rasterformat](https://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//009t0000000w000000)
* [FAQ: Was ist die Dateistruktur eines Arc/INFO Grids?](https://support.esri.com/en/technical-article/000008526)

