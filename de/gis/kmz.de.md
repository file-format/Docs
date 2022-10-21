{
  "date" : "2019-10-11",
  "keywords" :[ "kmz-Datei", "was ist eine kmz-Datei", "Datei", "kmz-Beispiel", "kmz-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - KML-ZIP-Dateiformat",
  "description":"Erfahren Sie mehr über das KMZ-Dateiformat und APIs, die KMZ-Dateien erstellen und öffnen können.",
  "linktitle" :"KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine KMZ-Datei?

Die KMZ-Datei (KML Zipped) ist eine Darstellung der gezippten [KML](/de/gis/kml/)-Datei, die Geoinformationen enthält, die in GIS-Anwendungen wie Google Earth angezeigt werden können. Informationen zu Ortsmarken werden in der Datei als Längen- und Breitengrad zusammen mit einem benutzerdefinierten Namen dargestellt. Die einzelne gepackte KMZ-Datei kann problemlos mit anderen Benutzern geteilt werden. KMZ-Dateien können auch 3D-Modelldaten für die Geodarstellung des Modells enthalten. Eine KMZ-Datei kann in Google Maps geöffnet werden, indem Sie die Datei an einem Online-Speicherort speichern und dann die URL in das Suchfeld von Google Maps eingeben.

## Dateistruktur ##

Der Inhalt einer MKZ-Datei besteht aus einer Haupt-KML-Datei und null oder mehr zugehörigen Dateien. Es kann mit einem standardmäßigen Dekomprimierungsprogramm wie WinZIP extrahiert werden. Das KMZ-Dateiformat wird ebenfalls zu einem Archiv mit einem Komprimierungsverhältnis von 10:1 komprimiert. Sie können Daten aus Google Earth-ähnlichen Anwendungen direkt in das KMZ-Dateiformat exportieren. Die Haupt-KML-Datei heißt **doc.kml**. Beim Packen einer KMZ-Datei können mehr als eine KML-Datei hinzugefügt werden, aber dies bringt keinen Vorteil, da Google Earth beim Öffnen der KMZ-Datei nach der ersten KML-Datei sucht und diese liest. Es ignoriert alle weiteren im Archiv gefundenen KML-Dateien. Um sicherzustellen, dass die gewünschte KML-Datei von Google Earth gelesen wird, wird empfohlen, nur eine einzige KML-Datei in die KMZ-Datei zu platzieren.

Die Bilder, Modelle, Texturen, Tondateien und andere Ressourcen, auf die in der Datei doc.kml verwiesen wird, werden in einem anderen Unterordner innerhalb des Hauptordners abgelegt. Dies kann je nach Anzahl der unterstützenden Dateien auch einige Komplexität mit sich bringen. Links zu diesen konstituierenden Ressourcen können relativ oder absolut referenziert werden.

### Relative Referenzierung ###

Wenn Ressourcen neben dem Hauptordner doc.kml in einem Unterordner innerhalb des Hauptordners platziert werden, kann die relative Referenzierung auf diese unterstützenden Dateien verweisen, wie im folgenden Beispiel gezeigt (nur für das Symbol).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Absolute Referenzierung ###

Ressourcen können auch absolut referenziert werden. Absolute Verweise enthalten die vollständige URL für die verlinkte Datei. Bei der Bereitstellung von Dateien auf einem zentralen Server stellt die absolute Referenzierung sicher, dass diese im Vergleich zur relativen Referenzierung eindeutig bleiben. Es wird nicht empfohlen, auf lokale Dateien absolut zu verweisen, da diese Links unterbrochen werden, wenn die Dateien auf ein neues System verschoben werden. Ein Beispiel für eine absolute Referenzierung ist wie folgt:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Siehe auch ##

* [GeoJSON](/de/gis/geojson/)

## Verweise ##

* [Google Earth und KMZ-Dateien](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

