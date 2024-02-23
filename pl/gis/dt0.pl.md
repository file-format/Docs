{
  "date": "2022-12-07",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Plik DT0 — format pliku DTED poziomu 0",
  "description": "Dowiedz się o formacie pliku DT0 i interfejsach API, które umożliwiają tworzenie i otwieranie plików DT0.",
  "linktitle": "DT0",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-dt-pl0"
}
},
  "lastmod": "2022-12-07"
}

## Czym jest plik DT0?

Plik DT0 to plik cyfrowych danych o wysokości terenu (DTED), który zawiera informacje poziomu 0 do badania danych o wysokości terenu. Dane dotyczące wysokości są równomiernie rozmieszczone w pliku DT0 i mogą być odczytywane przez popularne programy GIS, takie jak ESRI ArcGIS Pro, TatukGIS, Blue Marble Geographic Global Mapper i Pitney Bowes MapInfo. Pliki DT0 są najczęściej używane przez społeczności naukowe i techniczne do badania nachylenia, wzniesienia i chropowatości powierzchni terenów na całym świecie.

Format pliku DT0 jest podobny do typów plików [DT1](/gis/dt1/) i [DT2](/gis/dt2/), ale ma mniejszą szczegółowość.

### Format pliku DT0

Pliki DT0 zapisywane są jako pliki binarne na dysku. Można je odczytać za pomocą wielu aplikacji GIS. Pliki DT0 można połączyć w katalog rastrowy geobazy plików, którego można użyć do stworzenia jednej dużej mozaiki.

## Jak przekonwertować pliki rastrowe na DTED?

Istnieje wiele narzędzi, które umożliwiają konwersję plików rastrowych na pliki DTED. [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm) to jedno z takich narzędzi, które umożliwia konwersję rastra do formatu DTED.

## Bibliografia

 * [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm)
 * [Format pliku KML](/gis/kml/)

