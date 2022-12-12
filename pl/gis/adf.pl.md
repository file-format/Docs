{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - Binarny format siatki ESRI ArcInfo",
  "description":"Poznaj format pliku ADF i interfejsy API, które mogą tworzyć i otwierać pliki ADF.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Czym jest plik ADF?

Plik z rozszerzeniem .adf to format pliku danych rastrowych używany przez aplikacje ESRI, takie jak ArcGIS, ArcView i ArcInfo. Dane przestrzenne są przechowywane jako siatka binarna natywna dla ESRI. Siatka składa się z wierszy i kolumn komórek, które mogą być liczbami całkowitymi lub zmiennoprzecinkowymi. Siatki liczb całkowitych w pliku ADF reprezentują dane dyskretne, a siatki zmiennoprzecinkowe reprezentują dane ciągłe. Innym popularnym formatem plików ESRI jest plik [SHP](/pl/gis/shp/), który reprezentuje informacje geoprzestrzenne w postaci danych wektorowych, które mają być używane przez aplikacje systemów informacji geograficznej (GIS).

## Format pliku ADF — więcej informacji

Pliki ADF są zapisywane jako pliki binarne na dysku w siatce binarnej. Siatki liczb całkowitych mają atrybuty przechowywane w tabeli atrybutów wartości (VAT). Każda unikalna wartość w siatce ma jeden rekord w podatku VAT, w którym rekord przechowuje unikalną wartość, a liczba komórek w siatce jest reprezentowana przez tę wartość.

Siatki zmiennoprzecinkowe nie mają podatku VAT.

### Struktura siatki

Wewnątrz pliku ADF siatki są implementowane przy użyciu kafelkowej struktury danych rastrowych. Podstawową jednostką wewnątrz tej rastrowej struktury danych jest prostokątny blok komórek. Każdy blok jest przechowywany na dysku i kompresowany w strukturze pliku o zmiennej długości, zwanej kafelkiem. Każdy blok jest przechowywany jako jeden rekord o zmiennej długości.

Rastry GRID są przechowywane w obszarach roboczych, gdzie obszar roboczy zawiera jeden podkatalog informacyjny i podkatalog dla każdego GRID. Istnieje kilka plików, które zawierają dane dotyczące lokalizacji geograficznej i atrybutów dla odpowiedniej siatki. Podkatalog Info zawiera kilka plików, które przechowują pewne informacje o GRID i innych zestawach danych, takich jak pokrycie, w obszarze roboczym.

## Bibliografia ##

* [Format siatki ESRI](https://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//009t0000000w000000)
* [FAQ: Jaka jest struktura plików Arc/INFO Grid?](https://support.esri.com/en/technical-article/000008526)

