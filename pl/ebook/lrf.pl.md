{
  "date" : "2019-12-12",
  "keywords" :["LRF", "plik", "rozszerzenie", "format", "eBook", "Książka cyfrowa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku LRF i interfejsy API, które mogą tworzyć i otwierać pliki LRF.",
  "title" :"Format pliku LRF — plik przenośnego czytnika Sony",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Czym jest plik LRF?

Plik z rozszerzeniem .lrf to plik Broad Band eBook (BBeB), który zawiera dane dla Sony BBeB, w tym tekst, obrazy i dane dotyczące paginacji. Plik jest zapisywany w skompresowanym formacie binarnym, który zawiera nagłówek, określoną liczbę obiektów i indeks obiektów. Pliki LRF i LRX zawierają dwa dostępne formaty książek BBeB. Pliki LRF nie są szyfrowane i można je skompilować z plików [LRX](/pl/ebook/lrf/). Pliki LRF można konwertować z kilku innych typów plików, w tym PDF i HTML. Jeśli Twój komputer nie może otworzyć pliku LRF, to prawdopodobnie nie masz zainstalowanego oprogramowania do otwierania lub edycji plików LRF. Programy, które mogą otwierać pliki LRF, to Calibre, BookDesigner, Makelrf i Canon Book Creator dla systemu Windows, Calibre dla systemu Linux, Calibre i Sony Reader dla komputerów Macintosh.

## Krótka historia

Typ pliku LRF jest przede wszystkim kojarzony z Line Rider przez [inXile Entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). Line Rider to internetowa zabawka do fizyki, wynaleziona we wrześniu 2006 roku przez słoweńskiego studenta Boštjana Čadeža. Czytniki e-booków marki Sony (takie jak czytniki Sony PRS-500 i Sony Librie) wykorzystują rozszerzenie pliku LRF do swoich dokumentów i tekstów. Ten zastrzeżony typ pliku jest już przestarzały, podobnie jak powiązane pliki LRS i LRX. Te trzy typy plików tworzyły BroadBand eBook (BBeB), który został wycofany w 2010 roku, kiedy Sony zaczęło sprzedawać swoje ebooki w formacie EPUB.

## Format pliku LRF

Szczegółowe specyfikacje formatu plików LRF są dostępne w [archiwum internetowym] (https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). Plik LRF składa się z:
* nagłówek
* kilka obiektów
* indeks obiektu.

Wszystkie te wartości są w kolejności Intel (najpierw LSB).

### nagłówek LRF

|Przesunięcie (szesnastkowe) |Rozmiar (bajty) |Nazwa/znaczenie| Przykładowa wartość|
---|---|---|---|
|0 |8| Podpis LRF| 4C 00 52 00 46 00 00 00 = "LRF" w Unicode|
|8 |2| wersja?| 999 w większości plików|
|A |2| "Psuedo-szyfrowanie" |bajt klucza 48|
|0C |4| Identyfikator obiektu głównego| 0x0044|
|10 |8| LiczbaObiektów |342|
|18 |8| Przesunięcie indeksu obiektu| 0x00093440|
|20 |4| nieznany| 0|
|24 |1| Flagi| (16 - tył do przodu, 1 = przód do tyłu) 16|
|25 |1| nieznany |(dopełnienie?) 0|
|26 |2| nieznany| 1600|
|28 |2| nieznany| (wypełnienie?) 0|
|2A |2| Wysokość?| 600|
|2C |2| Szerokość?| 800|
|2E |1| nieznany| 24|
|2F |1| nieznany |(dopełnienie?) 0|
|30 |0x14| nieznany| zera|
|44 |4| Identyfikator obiektu tylko dla obiektu PlaneStream (0x1E)| 0x0042|
|48 |4| nieznany |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Bibliografia

* [Format pliku LRF] (https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB – z Wikipedii](https://en.wikipedia.org/wiki/BBeB)

