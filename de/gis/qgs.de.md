{
  "date" : "2019-10-11",
  "keywords" :[ "qgs-Datei", "qgs-Dateiformat", "was ist eine qgs-Datei", "Datei", "qgs-Beispiel", "qgs-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - QGIS-Projektdateiformat",
  "description":"Erfahren Sie mehr über das QGS-Dateiformat und APIs, die QGS-Dateien erstellen und öffnen können.",
  "linktitle" :"QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine QGS-Datei?

Eine Datei mit der Erweiterung .qgs ist eine Projektdatei, die mit [QGIS](https://www.qgis.org/en/site/) erstellt wurde, einer plattformübergreifenden Open-Source-GIS-Anwendung. Alle Projekteinstellungen wie Layereigenschaften und Hilfsdaten zum Projekt. Es wird erstellt, wenn ein Kartenprojekt auf einer Disc gespeichert wird. Es ist eigentlich eine Konfigurationsdatei, die Informationen wie Zeiger auf die GIS-Daten, Stilinformationen zu den Layern und den Projekttitel enthält. QGS-Dateien können mit QGIS-Software geöffnet werden, die kostenlos heruntergeladen werden kann.

## QGS-Dateiformat

QGS-Dateien haben das Format [XML](/de/web/xml/) und speichern Projektdaten als XML-Tags. Eine QGS-Datei enthält Informationen wie:

* Projekttitel
* Projekt CRS
* der Ebenenbaum
* Fangeinstellungen
* Beziehungen
* die Ausdehnung der Kartenleinwand
* Projektmodelle
* Legende
* Kartenansicht-Docks (2D und 3D)
* die Ebenen mit Links zu den zugrunde liegenden Datensätzen (Datenquellen) und anderen Ebeneneigenschaften, einschließlich Ausdehnung, SRS, Verbindungen, Stile, Renderer, Mischmodus, Deckkraft und mehr.
* Projekteigenschaften

### QGS-XML-Tags der obersten Ebene

{{< figure src="../qgstoplevel.png" title="" >}}

### Erweiterte Projektschicht-Tags der obersten Ebene

{{< figure src="../qgstoplevel.png" title="" >}}

## Verweise

* [QGIS](https://www.qgis.org/en/site/)

