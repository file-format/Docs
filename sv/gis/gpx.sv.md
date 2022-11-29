{
  "date" : "2019-10-11",
  "keywords" :[ "gpx-fil", "vad är en gpx-fil", "fil", "gpx-exempel", "gpx-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - GPX Exchange File Format",
  "description":"Läs mer om GPX-filformat och API:er som kan skapa och öppna GPX-filer.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en GPX fil?

Filer med GPX-tillägg representerar GPS Exchange-format för utbyte av GPS-data mellan applikationer och webbtjänster på internet. Det är ett lätt XML-filformat som innehåller GPS-data, dvs. waypoints, rutter och spår som ska importeras och röda av flera program. GPX-filformatet är öppet och stöds av olika applikationer och GPS-enheter. GPS-data från sådana filer kan laddas för visning i kartapplikationer för geospatiala ändamål.

## GPX-filformat ##

En GPX-fil består av platsdata för latitud och longitud, höjdvärden och annan eventuellt annan beskrivande information. Platsdata uttrycks som decimalgrader och höjden uttrycks i meter. Tiden i en GPX-fil är i Coordinated Universal Time (UTC) med ISO 8601-format. Fördelarna med att använda en GPX-fil är följande:

* GPX låter dig utbyta data med en växande lista med program för Windows, MacOS, Linux, Palm och PocketPC.
* GPX kan omvandlas till andra filformat med hjälp av en enkel webbsida eller omvandlingsprogram.
* GPX är baserat på XML-standarden, så många av de nya programmen du använder (till exempel Microsoft Excel) kan läsa GPX-filer.
* GPX gör det enkelt för alla på webben att utveckla nya funktioner som omedelbart fungerar med dina favoritprogram.

[GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) visar representationen av GPX-filformatet som referens.

### Viktiga data ###

Följande är viktiga data som är en del av en GPX-fil för representation av GPS-data.

* **Waypoints**: En waypoint är en WGS84 (GPS) koordinater för en punkt och representerar ett lager av funktioner av OGR-typ wkbPoint
* **Rutter**: Representerar ett lager av funktioner av OGR-typ wkbLineString. Den innehåller en lista över spårpunkter, som är vägpunkter som visar en sväng eller etapppunkter som leder till en destination
* **Spår**: Spår representerar ett lager av funktioner i OGR-typ wkbMultiLineString. Den består av minst ett segment som innehåller waypoints i en ordnad lista med punkter som beskriver en väg. Den består av en lista över spårpunkter som representerar ett kontinuerligt GPS-spår.

### GPX-exempelfil ###

Följande GPX-fil visar organisationen av GPS-data i en GPX-fil och kan ge en god uppfattning om innehållet i en GPX-fil.

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

## Referenser ##

* [GPX-filformat](http://www.topografix.com/gpx.asp)
* [GPX - av Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

