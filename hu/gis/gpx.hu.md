{
  "date" : "2019-10-11",
  "keywords" :[ "gpx fájl", "mi az a gpx fájl", "fájl", "gpx példa", "gpx fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - GPX Exchange fájlformátum",
  "description":"További információ a GPX fájlformátumról és az API-król, amelyek GPX-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a GPX fájl?

A GPX kiterjesztésű fájlok a GPS Exchange formátumot képviselik a GPS-adatok cseréjére az alkalmazások és az internetes webszolgáltatások között. Ez egy könnyű XML-fájlformátum, amely GPS-adatokat tartalmaz, azaz több program által importálandó útpontokat, útvonalakat és nyomvonalakat. A GPX fájlformátum nyitott, és számos alkalmazás és GPS-eszköz támogatja. Az ilyen fájlokból származó GPS-adatok betölthetők térinformatikai célú térképészeti alkalmazásokban való megjelenítéshez.

## GPX fájlformátum ##

A GPX-fájl szélességi és hosszúsági adatokból, magassági értékekből és egyéb, esetleg egyéb leíró információkból áll. A helyadatokat tizedes fokban, a magasságot méterben fejezik ki. A GPX-fájlokban az idő koordinált világidőben (UTC) van megadva, ISO 8601 formátumban. A GPX-fájlok használatának előnyei a következők:

* A GPX lehetővé teszi az adatok cseréjét a Windows, MacOS, Linux, Palm és PocketPC programok növekvő listájával.
* A GPX egy egyszerű weboldal vagy konvertáló program segítségével más fájlformátumokká alakítható.
* A GPX az XML szabványon alapul, így számos új program (például Microsoft Excel) képes olvasni a GPX fájlokat.
* A GPX bárki számára megkönnyíti az interneten olyan új funkciók kifejlesztését, amelyek azonnal működni fognak kedvenc programjaival.

A [GPX-séma](https://www.topografix.com/GPX/1/1/gpx.xsd) referenciaként mutatja be a GPX-fájlformátumot.

### Alapvető adatok ###

Az alábbiakban olyan alapvető adatok találhatók, amelyek egy GPX-fájl részét képezik a GPS-adatok megjelenítéséhez.

* **Útpontok**: Az útpont egy pont WGS84 (GPS) koordinátája, amely OGR típusú wkbPoint jellemzők rétegét képviseli.
* **Útvonalak**: A wkbLineString OGR típusú jellemzők rétegét képviselik. Tartalmazza a nyomvonalpontok listáját, amelyek olyan fordulópontok, amelyek egy kanyart vagy szakaszpontokat mutatnak, amelyek egy célhoz vezetnek
* **Tracks**: A sávok a wkbMultiLineString OGR típusú jellemzők rétegét képviselik. Legalább egy szegmensből áll, amely útvonalpontokat tartalmaz egy útvonalat leíró pontok rendezett listájában. A nyomvonalpontok listájából áll, amelyek egy folyamatos GPS nyomvonalat képviselnek.

### GPX példafájl ###

A következő GPX-fájl a GPS-adatok GPX-fájlban való elrendezését mutatja be, és jó képet ad a GPX-fájlok tartalmáról.

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

## Referenciák ##

* [GPX fájlformátum](https://www.topografix.com/gpx.asp)
* [GPX – a Wikipedia által](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

