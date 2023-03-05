{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku TCX — plik XML centrum szkoleniowego",
  "description":"Poznaj format pliku TCX i interfejsy API, które mogą tworzyć i otwierać pliki TCX.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Czym jest plik TCX?

Plik TCX (Training Center XML) to format wymiany danych używany do udostępniania danych między urządzeniami fitness. Został wprowadzony w 2008 roku wraz z produktem Garmin Training Center. Dane treningowe, takie jak tętno, rytm biegu, rytm roweru, kalorie i czas okrążenia, są przechowywane w formacie [XML](/pl/web/xml/) w pliku TCX. Ponadto w pliku TCX zawarte są również dane zbiorcze dotyczące ścieżki treningu. Pliki TCX są podobne do plików [FIT](/pl/gis/fit/), które są tworzone za pomocą sportowych urządzeń do noszenia firmy Garmin.

## Format pliku TCX — więcej informacji

Pliki TCX są zapisywane na dysku jako pliki XML, a każdy rekord jest zapisywany jako działanie. Aktywność obejmuje wszystkie dane treningu, takie jak czas, czas okrążenia, identyfikator, tętno, intensywność, rytm i informacje o trasie, które zawierają pary pozycji wraz ze znacznikiem czasu dla tej pozycji o szerokości geograficznej podobnej do [GPX](/pl/gis/gpx/).

### Wersje formatu plików TCX

Istnieją dwie wersje tego formatu z własnymi schematami XML hostowanymi przez firmę Garmin. Oto kilka z nich:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## Protokół danych TCX

Szybka wersja formatu TCX XML jest dostępna na Github jako [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Bibliografia ##

* [Centrum szkoleniowe XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [Przeglądarka TCX](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

