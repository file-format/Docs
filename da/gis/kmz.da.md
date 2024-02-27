{
  "date": "2019-10-11",
  "keywords": [
"kmz fil",
"hvad er en kmz-fil",
"fil",
"kmz eksempel",
"filtypenavnet kmz",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KMZ - KML zippet filformat",
  "description": "Lær om KMZ filformat og API'er, der kan oprette og åbne KMZ filer.",
  "linktitle": "KMZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-km-daz"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en KMZ fil?

KMZ (KML Zipped) fil er en repræsentation af zippet [KML](/gis/kml/) fil, der indeholder geospatial information, der kan ses i GIS-applikationer som Google Earth. Oplysninger om stedsmarkører er repræsenteret i filen som bredde- og længdegrad sammen med et brugerdefineret navn. Den enkelt pakkede KMZ-fil kan nemt deles med andre brugere. KMZ-filer kan også inkludere 3D-modeldata til geo-repræsentation af modellen. En KMZ-fil kan åbnes i Google Maps ved at gemme filen på en onlineplacering og derefter skrive URL'en i Google Maps-søgefeltet.

## Filstruktur ##

The contents of a MKZ file consist of a main KML file and zero or more associated files. It can be extracted using standard decompression utility like WinZIP. KMZ file format is also compressed to an archive with compression ratio of 10:1. Du kan eksportere data fra Google Earth som applikationer direkte til KMZ-filformat. Hoved-KML-filen hedder **doc.kml**. Mens du pakker en KMZ-fil, kan der tilføjes mere end én KML-fil til den, men det vil ikke være til nogen fordel, da Google Earth søger efter den første KML-fil, når du åbner KMZ-filen og læser den. Den ignorerer alle yderligere KML-filer, der findes i arkivet. For at være sikker på, at den ønskede KML-fil læses af Google Earth, anbefales det kun at placere en enkelt KML-fil i KMZ-filen.

Billederne, modellerne, teksturerne, lydfilerne og andre ressourcer, der refereres til i doc.kml-filen, placeres i en anden undermappe inde i hovedmappen. Dette kan også involvere en vis kompleksitet afhængigt af antallet af understøttende filer. Links til disse konstituerende ressourcer kan refereres relativt eller via absolut reference.

### Relativ reference ###

Når ressourcer placeres ved siden af hoved-doc.kml inde i en undermappe i hovedmappen, kan den relative henvisning pege på disse understøttende filer som vist i følgende eksempel (kun for ikon).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Absolut reference ###

Der kan også henvises til ressourcer. Absolutte referencer indeholder den fulde URL for den linkede fil. Når filer sendes på en central server, gør absolut reference det sikker på, at disse forbliver utvetydige sammenlignet med relative referencer. Lokal fil anbefales ikke at blive refereret til, da disse links vil bryde, når filerne flyttes til et nyt system. Et eksempel på absolut reference er som følger:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Se også ##

* [GeoJSON](/gis/geojson/)


## Referencer ##

* [Google Earth og KMZ-filer](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)


