{
  "date" : "2019-10-11",
  "keywords" :[ "plik gpx", "co to jest plik gpx", "plik", "przykład gpx", "rozszerzenie pliku gpx", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - format pliku wymiany GPX",
  "description":"Poznaj format plików GPX i interfejsy API, które mogą tworzyć i otwierać pliki GPX.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik GPX?

Pliki z rozszerzeniem GPX reprezentują format GPS Exchange do wymiany danych GPS między aplikacjami i usługami internetowymi w Internecie. Jest to lekki format pliku XML, który zawiera dane GPS, tj. punkty trasy, trasy i ślady, które mają być importowane i redagowane przez wiele programów. Format pliku GPX jest otwarty i jest obsługiwany przez różne aplikacje i urządzenia GPS. Dane GPS z takich plików można ładować do wyświetlania w aplikacjach mapujących do celów geoprzestrzennych.

## Format pliku GPX ##

Plik GPX składa się z danych dotyczących szerokości i długości geograficznej, wartości wysokości i innych ewentualnie innych informacji opisowych. Dane dotyczące lokalizacji są wyrażone w stopniach dziesiętnych, a wysokość w metrach. Czas w pliku GPX jest podany w uniwersalnym czasie koordynowanym (UTC) w formacie ISO 8601. Korzyści z używania pliku GPX są następujące:

* GPX umożliwia wymianę danych z rosnącą listą programów dla systemów Windows, MacOS, Linux, Palm i PocketPC.
* GPX można przekształcić w inne formaty plików za pomocą prostej strony internetowej lub programu konwertującego.
* GPX jest oparty na standardzie XML, więc wiele nowych programów, których używasz (na przykład Microsoft Excel) może odczytywać pliki GPX.
* GPX ułatwia każdemu w sieci opracowywanie nowych funkcji, które będą natychmiast współpracować z Twoimi ulubionymi programami.

[Schemat GPX](https://www.topografix.com/GPX/1/1/gpx.xsd) przedstawia reprezentację formatu pliku GPX w celach informacyjnych.

### Podstawowe dane ###

Poniżej przedstawiono podstawowe dane, które są częścią pliku GPX do reprezentacji danych GPS.

* **Punkty trasy**: Punkt trasy to współrzędne punktu WGS84 (GPS) reprezentujące warstwę obiektów typu OGR wkbPoint
* **Trasy**: Reprezentują warstwę obiektów typu OGR wkbLineString. Zawiera listę punktów trasy, które są punktami wskazującymi zwrot lub punkty etapowe, które prowadzą do miejsca docelowego
* **Ścieżki**: Ścieżki reprezentują warstwę cech typu OGR wkbMultiLineString. Składa się z co najmniej jednego segmentu zawierającego punkty nawigacyjne w uporządkowanej liście punktów opisujących ścieżkę. Składa się z listy punktów ścieżki, które reprezentują ciągłą ścieżkę GPS.

### Przykładowy plik GPX ###

Poniższy plik GPX pokazuje organizację danych GPS w pliku GPX i może dać dobre wyobrażenie o zawartości pliku GPX.

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

## Bibliografia ##

* [Format pliku GPX](https://www.topografix.com/gpx.asp)
* [GPX – z Wikipedii](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

