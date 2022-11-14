{
  "date" : "2019-10-11",
  "keywords" :[ "gpx-bestand", "wat is een gpx-bestand", "bestand", "gpx-voorbeeld", "gpx-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - GPX Exchange-bestandsindeling",
  "description":"Meer informatie over GPX-bestandsindelingen en API's die GPX-bestanden kunnen maken en openen.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een GPX-bestand?

Bestanden met de GPX-extensie vertegenwoordigen het GPS Exchange-formaat voor de uitwisseling van GPS-gegevens tussen applicaties en webservices op internet. Het is een lichtgewicht XML-bestandsformaat dat GPS-gegevens bevat, dwz waypoints, routes en tracks die door meerdere programma's moeten worden geïmporteerd en rood worden. GPX-bestandsindeling is open en wordt ondersteund door verschillende applicaties en GPS-apparaten. GPS-gegevens uit dergelijke bestanden kunnen worden geladen voor weergave op kaarttoepassingen voor georuimtelijke doeleinden.

## GPX-bestandsindeling ##

Een GPX-bestand bestaat uit locatiegegevens voor lengte- en breedtegraden, hoogtewaarden en andere mogelijk andere beschrijvende informatie. Locatiegegevens worden uitgedrukt in decimale graden en hoogte in meters. Tijd in een GPX-bestand is in Coordinated Universal Time (UTC) met behulp van ISO 8601-indeling. De voordelen van het gebruik van een GPX-bestand zijn als volgt:

* Met GPX kunt u gegevens uitwisselen met een groeiende lijst van programma's voor Windows, MacOS, Linux, Palm en PocketPC.
* GPX kan worden omgezet in andere bestandsindelingen met behulp van een eenvoudige webpagina of een conversieprogramma.
* GPX is gebaseerd op de XML-standaard, dus veel van de nieuwe programma's die je gebruikt (bijvoorbeeld Microsoft Excel) kunnen GPX-bestanden lezen.
* GPX maakt het voor iedereen op internet gemakkelijk om nieuwe functies te ontwikkelen die direct werken met uw favoriete programma's.

Het [GPX-schema](https://www.topografix.com/GPX/1/1/gpx.xsd) toont de weergave van het GPX-bestandsformaat ter referentie.

### Essentiële gegevens ###

Hieronder volgen essentiële gegevens die deel uitmaken van een GPX-bestand voor weergave van GPS-gegevens.

* **Waypoints**: een waypoint is een WGS84 (GPS)-coördinaten van een punt en vertegenwoordigt een laag met kenmerken van het OGR-type wkbPoint
* **Routes**: vertegenwoordigen een laag met kenmerken van het OGR-type wkbLineString. Het bevat een lijst met trackpunten, dit zijn waypoints die een afslag of etappepunten weergeven die naar een bestemming leiden
* **Tracks**: Tracks vertegenwoordigen een laag met kenmerken van het OGR-type wkbMultiLineString. Het bestaat uit ten minste één segment dat waypoints bevat in een geordende lijst van punten die een pad beschrijven. Het bestaat uit een lijst met trackpunten die een continue GPS-track vertegenwoordigen.

### GPX-voorbeeldbestand ###

Het volgende GPX-bestand toont de organisatie van GPS-gegevens in een GPX-bestand en kan een goed beeld geven van de inhoud van een GPX-bestand.

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

## Referenties ##

* [GPX-bestandsindeling](http://www.topografix.com/gpx.asp)
* [GPX - Door Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

