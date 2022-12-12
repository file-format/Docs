{
  "date" : "2021-07-29",
  "keywords" :[ "plik shx", "format pliku shx", "co to jest plik shx", "plik", "przykład shx", "rozszerzenie pliku shx", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX — format indeksu kształtu pliku kształtu",
  "description":"Poznaj format pliku SHX i interfejsy API, które mogą tworzyć i otwierać pliki SHX.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Czym jest plik SHX?
Plik SHX należy do formatu indeksu kształtu, który jest indeksem pozycyjnym geometrii obiektu, umożliwiającym szybkie wyszukiwanie do przodu i do tyłu. SHX to plik offsetowy z bezpośrednim dostępem. W tym pliku nie ma żadnych danych, tylko duplikat pierwszych stu bajtów, numer rekordu i przesunięcie do początkowego bajtu tego rekordu w shp. Należy pamiętać, że plik z rozszerzeniem .shx nie łączy [SHP](/pl/gis/shp) i [DBF](/pl/database/dbf).

## Format pliku SHX
Format SHX zawiera indeks pozycyjny geometrii elementu i 100-bajtowy nagłówek podobny do pliku SHP, po którym następuje dowolna liczba 8-bajtowych rekordów o stałej długości, które zawierają następujące dwa pola:
| Bajty | Wpisz | endianizm | Użycie |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | duży | Przesunięcie rekordu (w słowach 16-bitowych) |
| 4–7 | int32 | duży | Długość rekordu (w słowach 16-bitowych) |

Indeks ten umożliwia wyszukiwanie wstecz w pliku kształtu poprzez najpierw wyszukiwanie wstecz w indeksie kształtu, a następnie odczytywanie przesunięcia rekordu. Tego przesunięcia można użyć do wyszukania właściwej pozycji w pliku SHP. Możesz także szukać napastników; dowolną liczbę rekordów przy użyciu tej samej metody. Chociaż możliwe jest wygenerowanie pełnego indeksu wraz z plikiem SHP, może to jednak zwiększyć szanse na szybkie uszkodzenie pliku SHP.


## Bibliografia

* [Shapefile – z Wikipedii)](https://en.wikipedia.org/wiki/Shapefile)


