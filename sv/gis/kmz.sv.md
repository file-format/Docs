{
  "date" : "2019-10-11",
  "keywords" :[ "kmz fil", "vad är en kmz fil", "fil", "kmz exempel", "kmz filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - KML zippad filformat",
  "description":"Läs mer om KMZ-filformat och API:er som kan skapa och öppna KMZ-filer.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en KMZ fil?

KMZ-fil (KML Zipped) är en representation av zippad [KML](/sv/gis/kml/)-fil som innehåller geospatial information som kan visas i GIS-applikationer som Google Earth. Information om platsmärken representeras i filen som latitud och longitud tillsammans med ett anpassat namn. Den enda paketerade KMZ-filen kan enkelt delas med andra användare. KMZ-filer kan även innehålla 3D-modelldata för geo-representation av modellen. En KMZ-fil kan öppnas i Google Maps genom att spara filen på en plats online och sedan skriva in webbadressen i sökrutan i Google Maps.

## Filstruktur ##

Innehållet i en MKZ-fil består av en huvud-KML-fil och noll eller fler associerade filer. Det kan extraheras med hjälp av standard dekompressionsverktyg som WinZIP. KMZ-filformatet komprimeras också till ett arkiv med komprimeringsförhållandet 10:1. Du kan exportera data från Google Earth som applikationer direkt till KMZ-filformat. Huvud-KML-filen heter **doc.kml**. När du packar en KMZ-fil kan mer än en KML-fil läggas till i den, men det kommer inte att vara till någon nytta eftersom Google Earth söker efter den första KML-filen när du öppnar KMZ-filen och läser den. Den ignorerar alla ytterligare KML-filer som finns i arkivet. För att vara säker på att den önskade KML-filen läses av Google Earth, rekommenderas endast en enda KML-fil att placeras i KMZ-filen.

Bilderna, modellerna, texturerna, ljudfilerna och andra resurser som refereras till i doc.kml-filen placeras i en annan undermapp i huvudmappen. Detta kan också innebära viss komplexitet beroende på antalet stödfiler. Länkar till dessa ingående resurser kan refereras relativt eller via absolut referens.

### Relativ referens ###

När resurser placeras bredvid huvuddokumentet.kml i en undermapp i huvudmappen, kan den relativa hänvisningen peka på dessa stödfiler som visas i följande exempel (endast för ikon).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Absolut referens ###

Resurser kan absolut också refereras. Absoluta referenser innehåller den fullständiga URL:en för den länkade filen. När filer läggs ut på en central server, gör absolut referens det säkert att dessa förblir entydiga jämfört med relativa referenser. Lokal fil rekommenderas inte att refereras absolut eftersom dessa länkar kommer att gå sönder när filerna flyttas till ett nytt system. Ett exempel på absolut referens är följande:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Se även ##

* [GeoJSON](/sv/gis/geojson/)

## Referenser ##

* [Google Earth och KMZ-filer](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

