{
  "date" : "2019-10-11",
  "keywords" :["plik qgs", "format pliku qgs", "co to jest plik qgs", "plik", "przykład qgs", "rozszerzenie pliku qgs", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - Format pliku projektu QGIS",
  "description":"Dowiedz się o formacie plików QGS i interfejsach API, które mogą tworzyć i otwierać pliki QGS.",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik QGS?

Plik z rozszerzeniem .qgs to plik projektu utworzony za pomocą [QGIS](https://www.qgis.org/en/site/), który jest wieloplatformową aplikacją GIS typu open source. Wszystkie ustawienia projektu, takie jak właściwości warstw i dane pomocnicze dla projektu. Jest tworzony, gdy projekt mapy jest zapisywany na dysku. W rzeczywistości jest to plik konfiguracyjny, który przechowuje informacje, takie jak wskaźniki do danych GIS, informacje o stylach warstw i tytuł projektu. Pliki QGS można otwierać za pomocą oprogramowania QGIS, które można bezpłatnie pobrać.

## Format pliku QGS

Pliki QGS są w formacie [XML](/pl/web/xml/) i przechowują dane projektów jako znaczniki XML. Plik QGS zawiera informacje, takie jak:

* Tytuł Projektu
*projekt CRS
* drzewo warstw
* Ustawienia przyciągania
* relacje
* zasięg płótna mapy
* modele projektów
* legenda
* doki mapview (2D i 3D)
* Warstwy z linkami do podstawowych zestawów danych (źródeł danych) i innych właściwości warstw, w tym zasięgu, SRS, połączeń, stylów, renderowania, trybu mieszania, krycia i innych.
* właściwości projektu

### Znaczniki XML najwyższego poziomu QGS

{{< figure src="../qgstoplevel.png" title="" >}}

### Rozszerzone znaczniki warstw projektu najwyższego poziomu

{{< figure src="../qgstoplevel.png" title="" >}}

## Bibliografia

* [QGIS](https://www.qgis.org/en/site/)

