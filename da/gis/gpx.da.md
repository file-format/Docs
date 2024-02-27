{
  "date": "2019-10-11",
  "keywords": [
"gpx fil",
"hvad er en gpx-fil",
"fil",
"gpx eksempel",
"gpx filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GPX - GPX Exchange-filformat",
  "description": "Lær om GPX-filformat og API'er, der kan oprette og åbne GPX-filer.",
  "linktitle": "GPX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gp-dax"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en GPX fil?

Filer med GPX-udvidelse repræsenterer GPS Exchange-format til udveksling af GPS-data mellem applikationer og webtjenester på internettet. Det er et letvægts XML-filformat, der indeholder GPS-data, dvs. waypoints, ruter og spor, der skal importeres og rødt af flere programmer. GPX-filformatet er åbent og understøttes af forskellige applikationer og GPS-enheder. GPS-data fra sådanne filer kan indlæses til visning på kortapplikationer til geospatiale formål.

## GPX-filformat ##

En GPX-fil består af placeringsdata for breddegrad og længdegrad, højdeværdier og andre muligvis andre beskrivende oplysninger. Lokalitetsdata er udtrykt som decimalgrader, og højde er udtrykt i meter. Tiden i en GPX-fil er i Coordinated Universal Time (UTC) ved brug af ISO 8601-format. Fordelene ved at bruge en GPX-fil er som følger:

* GPX giver dig mulighed for at udveksle data med en voksende liste af programmer til Windows, MacOS, Linux, Palm og PocketPC.

* GPX kan omdannes til andre filformater ved hjælp af en simpel webside eller et konverterprogram.

* GPX er baseret på XML-standarden, så mange af de nye programmer du bruger (Microsoft Excel f.eks.) kan læse GPX-filer.

* GPX gør det nemt for alle på nettet at udvikle nye funktioner, som med det samme vil fungere sammen med dine yndlingsprogrammer.


[GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) viser repræsentationen af GPX-filformatet til reference.

### Væsentlige data ###

Følgende er væsentlige data, der er en del af en GPX-fil til repræsentation af GPS-data.

* **Waypoints**: Et waypoint er en WGS84 (GPS) koordinater for et punkt og repræsenterer lag af funktioner af OGR-typen wkbPoint

* **Ruter**: Repræsenterer et lag af funktioner af OGR-typen wkbLineString. Det inkluderer en liste over sporpunkter, som er waypoints, der viser et sving eller etapepunkter, der fører til en destination

* **Spor**: Spor repræsenterer lag af funktioner af OGR-typen wkbMultiLineString. Den er lavet af mindst et segment, der indeholder waypoints i en ordnet liste over punkter, der beskriver en sti. Den består af en liste over sporpunkter, som repræsenterer et kontinuerligt GPS-spor.


### GPX Eksempel fil ###

Den følgende GPX-fil viser organiseringen af GPS-data i en GPX-fil og kan give en god idé om indholdet af en GPX-fil.

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

## Referencer ##

* [GPX-filformat](https://www.topografix.com/gpx.asp)

* [GPX - af Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)


