{
  "date" : "2019-10-11",
  "keywords" :["plik b6z", "format pliku b6z", "co to jest plik b6z", "plik", "przykład b6z", "rozszerzenie pliku b6z","rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku archiwum B6Z - B6ZIP",
  "description":"Poznaj format pliku B6Z i interfejsy API, które mogą tworzyć i otwierać pliki B6Z.",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Czym jest plik B6Z?

Plik z rozszerzeniem .b6z to skompresowany plik archiwum utworzony przez aplikację macOS [B6Zip] (http://b6zip.com), która służy do kompresji i dekompresji plików. Jest to stosunkowo nowy format archiwum, który umożliwia wyższy stopień kompresji. B6Z ma otwartą architekturę i obsługuje rozmiary plików do 900000 PB. Obsługuje kompresję danych, odzyskiwanie błędów i łączenie plików. Oprogramowanie narzędziowe B6Zip jest dostępne bezpłatnie w systemie MacOS do otwierania różnych typów skompresowanych plików, w tym B6Z.

## Format pliku B6Z

Format pliku B6Z jest oparty na otwartej architekturze i zapewnia solidną kompresję z algorytmem szyfrowania AES-256. Wykorzystuje LZMA2 jako domyślną metodę kompresji, ale obsługuje również inne metody kompresji, jak poniżej.

|Metoda|Opis|
---|---|
|LZMA |Zoptymalizowana wersja algorytmu LZ77|
|LZMA2| Ulepszona wersja LZMA|
|Spuść powietrze| Zwykły algorytm LZ77|
|BZip2| Standardowy algorytm BWT|
|PPMD| PPMdH| Dmitrija Shkarina

Narzędzie B6Zip obsługuje wszystkie te standardy kompresji i jest wysoce zoptymalizowane, co zapewnia dużą prędkość. Obsługuje pracę z formatami plików [ZIP](/pl/compression/zip/), [TAR](/pl/compression/tar/) i [RAR](/pl/compression/rar/). Pliki B6Z mają aplikację typu MIME/x-b6z-skompresowaną.

## Bibliografia

* [B6Zip](http://b6zip.com)

