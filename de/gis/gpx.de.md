{
  "date" : "2019-10-11",
  "keywords" :[ "gpx-Datei", "was ist eine gpx-Datei", "Datei", "gpx-Beispiel", "gpx-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - GPX-Austauschdateiformat",
  "description":"Erfahren Sie mehr über das GPX-Dateiformat und APIs, die GPX-Dateien erstellen und öffnen können.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine GPX-Datei?

Dateien mit der Erweiterung GPX stellen das GPS-Austauschformat für den Austausch von GPS-Daten zwischen Anwendungen und Webdiensten im Internet dar. Es ist ein leichtes XML-Dateiformat, das GPS-Daten enthält, dh Wegpunkte, Routen und Tracks, die importiert und von mehreren Programmen gelesen werden können. Das GPX-Dateiformat ist offen und wird von einer Vielzahl von Anwendungen und GPS-Geräten unterstützt. GPS-Daten aus solchen Dateien können zur Anzeige in Kartierungsanwendungen für georäumliche Zwecke geladen werden.

## GPX-Dateiformat ##

Eine GPX-Datei besteht aus Breiten- und Längengrad-Standortdaten, Höhenwerten und anderen möglicherweise anderen beschreibenden Informationen. Positionsdaten werden in Dezimalgrad und die Höhe in Metern ausgedrückt. Die Zeit in einer GPX-Datei wird in der koordinierten Weltzeit (UTC) im ISO 8601-Format angegeben. Die Vorteile der Verwendung einer GPX-Datei sind wie folgt:

* Mit GPX können Sie Daten mit einer wachsenden Liste von Programmen für Windows, MacOS, Linux, Palm und PocketPC austauschen.
* GPX kann mit einer einfachen Webseite oder einem Konvertierungsprogramm in andere Dateiformate umgewandelt werden.
* GPX basiert auf dem XML-Standard, sodass viele der neuen Programme, die Sie verwenden (z. B. Microsoft Excel), GPX-Dateien lesen können.
* GPX macht es jedem im Internet leicht, neue Funktionen zu entwickeln, die sofort mit Ihren Lieblingsprogrammen funktionieren.

Das [GPX-Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) zeigt die Darstellung des GPX-Dateiformats als Referenz.

### Wesentliche Daten ###

Es folgen wesentliche Daten, die Teil einer GPX-Datei zur Darstellung von GPS-Daten sind.

* **Wegpunkte**: Ein Wegpunkt ist eine WGS84 (GPS)-Koordinate eines Punktes und stellt eine Schicht von Merkmalen des OGR-Typs wkbPoint dar
* **Routen**: Repräsentieren eine Schicht von Merkmalen des OGR-Typs wkbLineString. Es enthält eine Liste von Trackpunkten, bei denen es sich um Wegpunkte handelt, die eine Abbiegung oder Etappenpunkte zeigen, die zu einem Ziel führen
* **Tracks**: Tracks stellen Layer von Features des OGR-Typs wkbMultiLineString dar. Es besteht aus mindestens einem Segment, das Wegpunkte in einer geordneten Liste von Punkten enthält, die einen Weg beschreiben. Es besteht aus einer Liste von Trackpunkten, die einen kontinuierlichen GPS-Track darstellen.

### GPX-Beispieldatei ###

Die folgende GPX-Datei zeigt die Organisation von GPS-Daten in einer GPX-Datei und kann eine gute Vorstellung über den Inhalt einer GPX-Datei geben.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## Verweise ##

* [GPX-Dateiformat](http://www.topografix.com/gpx.asp)
* [GPX – von Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

