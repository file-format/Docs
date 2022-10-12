{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "Datei", "Erweiterung", "Dateiformat", "GPS-Standort", "Wegpunkt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - GPS-Standortdateiformat",
  "description":"Erfahren Sie mehr über das LOC-Dateiformat und APIs, die LOC-Dateien erstellen und öffnen können.",
  "linktitle" :"LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## Was ist eine LOC-Datei?

Eine Datei mit der Erweiterung .loc ist eine GPS-Standortdatei, die Geostandorte als Wegpunkte enthält. Ein Wegpunkt ist ein Paar von Breitengrad- und Längengradwerten, das sich auf einen Standort bezieht, der von GIS-Anwendungen (Geographical Information System) verwendet wird. GPS-Mapping-Programme wie DeLorme Topo verwenden LOC-Dateien zum Lesen und Anzeigen von Informationen, die in diesen LOC-Dateien enthalten sind, als auswählbare Schichten durch Endbenutzer. Darüber hinaus dienen diese dazu, GPS-Daten zwischen Anwendungen auszutauschen. LOC-Dateien können mit Anwendungen wie [TopoGrafix EasyGPS](https://www.easygps.com/) geöffnet werden, die den Inhalt solcher Dateien als Layer und Daten anzeigen, die auf der Karte an der jeweiligen Geolokalisierung dargestellt sind.

## LOC-Dateiformat – Weitere Informationen

LOC-Dateien haben Ähnlichkeiten mit [GPX](/de/gis/gpx/)-Dateien, werden aber in einem anderen Format gespeichert. Diese werden als [XML](/de/web/xml/)-Dateien gespeichert, in denen der Inhalt von Wegpunkten und zugehörigen Informationen in strukturierten Tags enthalten sind. Da XML eine verallgemeinerte Sprache zum Austausch von Daten zwischen verschiedenen Anwendungen ist, erleichtert dies den Austausch von LOC-Daten mit anderen Anwendungen.

## LOC-Dateiformat – Beispiel

Es folgt die Überschrift und der Text eines Wegpunkts aus einer LOC-Datei. Wie zu sehen ist, enthalten die Header-Informationen die Ortsquelle für die Daten. Der Wegpunkt enthält Informationen wie die ,ID' und zugehörige Inhaltsdaten, die dem Wegpunkt zugeordnet sind. Schließlich ist der Wegpunkt eine Sammlung von Breiten- und Längengradwerten und dem Text, der diesem bestimmten Wegpunkt zugeordnet ist.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Verweise

* [TopGraphic EasyGPS](https://www.easygps.com/)

