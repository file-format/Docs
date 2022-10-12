{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPG-Dateiformat - ESRI Codepage-Datei",
  "description":"Erfahren Sie mehr über das CPG-Dateiformat und APIs, die CPG-Dateien erstellen und öffnen können.",
  "linktitle" :"CPG",
  "menu" : {
    "docs" : {
"identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## Was ist eine CPG-Datei?

Eine CPG-Datei ist eine optionale Datei, die für das ESRI Shapefile erforderlich ist, das verwendet wird, um die Codepage zum Identifizieren des zu verwendenden Zeichensatzes anzugeben. Diese werden im Nur-Text-Dateiformat gespeichert und enthalten Informationen über die Codierung, die zum Erstellen des Shapefiles verwendet wurde. Falls keine CPG-Datei verfügbar ist, verwendet das Shapefile die Standardcodierung des Systems. Eine CPG-Datei, falls vorhanden, muss das gleiche Präfix wie das der [SHP](/de/gis/shp/)-Datei haben, zum Beispiel road.shp, road.cpg.

CPG-Dateien können mit ESRI ArcGIS Pro geöffnet werden.

### CPG-Dateiformat - Weitere Informationen

Wenn Sie ein Shapefile in ArcCatalog oder einer anderen ArcGIS-Anwendung anzeigen, sehen Sie nur das Shapefile. In Wirklichkeit verwendet Shapefile jedoch andere zugehörige Dateien, die neben der Haupt-Shape-Datei gelesen werden. Die CPG-Datei ist auch eine davon, wenn sie neben der Haupt-SHP-Datei vorhanden ist.

## Verweise

* [Shapefile-Dateierweiterungen
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

