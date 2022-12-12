{
  "date" : "2021-07-29",
  "keywords" :[ "plik gpkg", "format pliku gpkg", "co to jest plik gpkg", "plik", "przykład gpkg", "rozszerzenie pliku gpkg", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - Pliki w formacie GeoPackage",
  "description":"Dowiedz się o formacie pliku GPKG i interfejsach API, które mogą tworzyć i otwierać pliki GPKG.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Czym jest plik GPKG?
Plik z rozszerzeniem .gpkg składa się z systemu informacji geograficznej zaimplementowanego jako kontener bazy danych SQLite zawierający tabele danych i metadanych z typowymi definicjami, ograniczeniami formatu, zapewnieniami integralności i ograniczeniami treści. Został opublikowany w 2014 roku; zdefiniowane przez OGC (Open Geospatial Consortium) w imieniu armii USA. Różne rządy, organizacje komercyjne i open source szeroko wspierają GeoPackage.

## Format pliku GPKG
GeoPackage składa się z rozszerzonego pliku bazy danych SQLite 3; norma określa zbiór zasad (wymaganych konwencji) dotyczących:
- Przechowywanie zestawów matryc płytek obrazów
- Funkcje wektorowe
- Mapy rastrowe w różnych skalach
- Metadane i schemat

Możesz rozszerzyć GeoPackage, korzystając z zasad rozszerzania określonych w punkcie 2.3 normy. Celem zaprojektowania GeoPackage było stworzenie jak najbardziej lekkiej bazy danych i umieszczenie jej w jednym, gotowym do użycia pliku. To sprawia, że idealnie nadaje się do aplikacji mobilnych w trybie off-line i szybkiego udostępniania w chmurze lub urządzeniach pamięci masowej USB itp.

### Zawartość GPKG
GeoPackages zawierają pewną liczbę tabel, podobnie jak inne relacyjne bazy danych. Tabele te mogą być tabelami zdefiniowanymi przez użytkownika lub tabelami metadanych. GeoPackages składają się z dwóch obowiązkowych tabel metadanych:

#### gpkg_contents
Spis treści dla GeoPackage. Obowiązkowe kolumny w tej tabeli to:

- **nazwa_tabeli**: rzeczywista nazwa tabeli danych zdefiniowanej przez użytkownika;
- **data_type**: typ danych, np. tytuły, cechy i atrybuty;
- **identyfikator i opis**: tekst czytelny dla człowieka;
- **last_change**: informacyjna data ostatniej zmiany, w formacie ISO 8601;
- **min_x, min_y, max_x i max_y**: zasięg przestrzenny treści. ;
- **srs_id**: przestrzenny układ odniesienia .

#### gpkg_spatial_ref_sys
W przypadku treści odniesienia przestrzennego; w tym między innymi kafelki i funkcje, każdy wiersz w treści musi odwoływać się do systemu odniesienia za pomocą współrzędnych; przechowywane w tabeli **gpkg_spatial_ref_sys**. Obowiązkowe kolumny w tej tabeli to:

- **nazwa_srs, opis**: czytelna dla człowieka nazwa i opis SRS;
- **srs_id**: unikalny identyfikator SRS; także klucz podstawowy tabeli;
- **organizacja**: bez rozróżniania wielkości liter nazwa organizacji definiującej.
- **organization_coordsys_id**: Numeryczny identyfikator SRS przypisany przez organizację;
- **definicja**: dobrze znana definicja tekstu SRS.


## Bibliografia

* [GeoPackage - z Wikipedii)](https://en.wikipedia.org/wiki/GeoPackage)
* [Pierwsze kroki z GeoPackage](http://www.geopackage.org/guidance/getting-started.html)

