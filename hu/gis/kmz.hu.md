{
  "date" : "2019-10-11",
  "keywords" :[ "kmz fájl", "mi az a kmz fájl", "fájl", "kmz példa", "kmz fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ – KML tömörített fájlformátum",
  "description":"További információ a KMZ fájlformátumról és az API-król, amelyek KMZ-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a KMZ fájl?

A KMZ (KML Zipped) fájl a tömörített [KML](/hu/gis/kml/) fájl reprezentációja, amely térinformatikai információkat tartalmaz, amelyek a GIS-alkalmazásokban, például a Google Earthben megtekinthetők. A helyjelzőkkel kapcsolatos információk a fájlban szélességi és hosszúsági fokként, valamint egyéni névként jelennek meg. Az egyetlen csomagolt KMZ-fájl könnyen megosztható más felhasználókkal. A KMZ-fájlok 3D-s modelladatokat is tartalmazhatnak a modell földrajzi megjelenítéséhez. A KMZ-fájl úgy nyitható meg a Google Térképen, hogy elmenti a fájlt egy online helyre, majd beírja az URL-t a Google Térkép keresőmezőjébe.

## Fájlszerkezet ##

Az MKZ-fájlok tartalma egy fő KML-fájlból és nulla vagy több kapcsolódó fájlból áll. Kibontható szabványos kicsomagoló segédprogrammal, mint például a WinZIP. A KMZ fájlformátum is 10:1-es tömörítési arányú archívummá van tömörítve. A Google Földből, például alkalmazásokból adatokat exportálhat közvetlenül KMZ fájlformátumba. A fő KML-fájl neve **doc.kml**. A KMZ-fájl csomagolása közben egynél több KML-fájl is hozzáadható hozzá, de ez nem lesz előnyös, mivel a Google Earth a KMZ-fájl megnyitásakor megkeresi az első KML-fájlt, és beolvassa azt. Figyelmen kívül hagyja az archívumban talált további KML-fájlokat. Annak érdekében, hogy a kívánt KML-fájlt biztosan beolvassa a Google Föld, csak egyetlen KML-fájlt ajánlatos elhelyezni a KMZ-fájlban.

A doc.kml fájlban hivatkozott képek, modellek, textúrák, hangfájlok és egyéb források a főmappán belül egy másik almappába kerülnek. Ez némi bonyolultsággal is járhat, a támogató fájlok számától függően. Az ezekre az alkotóelemekre mutató hivatkozások vonatkozhatnak relatíve vagy abszolút hivatkozáson keresztül.

### Relatív hivatkozás ###

Ha az erőforrásokat a fő doc.kml mellett helyezik el a főmappán belüli almappában, a relatív hivatkozás ezekre a támogató fájlokra mutathat, amint az a következő példában látható (csak ikon esetén).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Abszolút hivatkozás ###

A forrásokra abszolút hivatkozni lehet. Az abszolút hivatkozások tartalmazzák a hivatkozott fájl teljes URL-címét. Amikor a fájlok egy központi szerverre kerülnek fel, az abszolút hivatkozás biztosítja, hogy ezek egyértelműek maradjanak a relatív hivatkozásokhoz képest. A helyi fájlokra nem ajánlott feltétlenül hivatkozni, mivel ezek a hivatkozások megszakadnak, amikor a fájlokat áthelyezik egy új rendszerbe. Egy példa az abszolút hivatkozásra a következő:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Lásd még ##

* [GeoJSON](/hu/gis/geojson/)

## Referenciák ##

* [Google Föld és KMZ-fájlok](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

