{
  "date" : "2019-10-11",
  "keywords" :[ "kml-Datei", "was ist eine kml-Datei", "Datei", "kml-Beispiel", "kml-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Schlüsselloch-Auszeichnungssprache",
  "description":"Erfahren Sie mehr über das KML-Dateiformat und APIs, die KML-Dateien erstellen und öffnen können.",
  "linktitle" :"KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine KML-Datei?

KML, Keyhole Markup Language) enthält Geoinformationen in XML-Notation. Als KML gespeicherte Dateien können in GIS-Anwendungen (Geographic Information System) geöffnet werden, sofern diese dies unterstützen. Viele Anwendungen haben damit begonnen, das KML-Dateiformat zu unterstützen, nachdem es als internationaler Standard angenommen wurde. KML verwendet eine Tag-basierte Struktur mit verschachtelten Elementen und Attributen. Bei allen Tags wird zwischen Groß- und Kleinschreibung unterschieden, und es ist wichtig, die Reihenfolge dieser Tags gemäß der [KML](https://developers.google.com/kml/documentation/kmlreference)-Referenz einzuhalten.

## Kurze Geschichte ##

KML wurde ursprünglich für die Verwendung mit Google Earth entwickelt, das ursprünglich als Keyhole Earth Viewer bekannt war. KLM wurde 2008 vom Open Geospatial Consortium als internationaler Standard übernommen. Da das Format für die Verwendung mit Google Earth entwickelt wurde, zeichnet es sich dadurch aus, dass es das erste ist, das KML-Dateien anzeigen und bearbeiten kann. Im Laufe der Zeit gibt es nun immer mehr Projekte, die Unterstützung für KML-Dateiformate einschließlich mehrerer APIs in verschiedenen Sprachen bieten.

## KML-Dateiformatspezifikationen ##

Die KML-Referenz ist eine vollständige Anleitung zum Nachschlagen, um die vollständigen Dateiformatspezifikationen zu erhalten. Eine Standard-KML-Datei besteht aus:

* Ortsmarken
* Beschreibendes HTML in Ortsmarken
* Bodenauflagen
* Pfade
* Polygone

Darüber hinaus kann eine erweiterte Version der KML-Datei Folgendes enthalten:

* Stile für Geometrie
* Stile für hervorgehobene Symbole
* Bildschirmüberlagerungen
* Netzwerk-Links

Jedes der KML-Elemente enthält Lat-Long-Informationen, die die in der Datei vorhandenen Informationen geolokalisieren. Es können jedoch auch zusätzliche Parameter wie Kurs, Höhe und Neigung vorhanden sein.

### Ortsmarken ###

Es wird verwendet, um eine Position auf der Erdoberfläche darzustellen und wird durch das gekennzeichnet<Point> Element. Nachfolgend sehen Sie ein Beispiel, wie eine Ortsmarke in einer KML-Datei dargestellt wird.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### Beschreibendes HTML in Ortsmarken ###

Einer Ortsmarke können zusätzliche Informationen zugeordnet werden, die die Darstellung der Ortsmarke weiter verbessern. Zu diesen Informationen gehören Links, Schriftgrößen, Stile und Farben. Darüber hinaus enthält es auch Textausrichtung und Tabellen als Teil der Ortsmarkierung.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### Bodenauflagen ###

Diese stellen die Schichtung eines Bildes auf der Erdoberfläche dar. Das<icon> Element enthält den Link zur Overlay-Bilddatei.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### Pfade ###

Pfade werden dargestellt durch<LineString> Element, das eine Sammlung von Lat-Long-Paaren ist. Mit diesen lassen sich in Google Earth viele verschiedene Arten von Wegen erstellen.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## Raumbezug in KML-Datei ##

Informationen, die in Geodatendateien über Geo-Standorte enthalten sind, können ohne räumliche Referenzinformationen unterschiedliche Bedeutungen haben. Standardmäßig wird die räumliche Referenzierung von KML-Dateien durch das World Geodetic System von 1984, WGS84, definiert.

## Verweise ##

* [KML-Referenz](https://developers.google.com/kml/documentation/kmlreference)
* [Google Developer Tutorial für KML](https://developers.google.com/kml/documentation/kml_tut)
* [KML-Dateiformat](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

