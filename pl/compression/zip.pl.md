{
  "date" : "2019-12-09",
  "keywords" :[ "plik zip", "format pliku zip", "co to jest plik zip", "plik", "przykład zip", "rozszerzenie pliku zip", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZAMEK BŁYSKAWICZNY",
  "description":"Co to jest plik ZIP i interfejsy API, które mogą tworzyć i otwierać pliki ZIP.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Co to jest plik ZIP? ##

Plik z rozszerzeniem .zip to archiwum, które może zawierać jeden lub więcej plików lub katalogów. W archiwum można zastosować kompresję dołączonych plików w celu zmniejszenia rozmiaru pliku ZIP. Format pliku ZIP został upubliczniony w lutym 1989 roku przez Phila Katza w celu archiwizacji plików i folderów. Format stał się częścią narzędzia [PKZIP](https://www.pkware.com/pkzip), stworzonego przez PKWARE, Inc. Zaraz po udostępnieniu [dostępnych specyfikacji](https://pkware.cachefly.net/ webdocs/casestudies/APPNOTE.TXT), wiele firm uczyniło format pliku ZIP częścią swojego oprogramowania narzędziowego, w tym Microsoft (od Windows 7), Apple (Mac OS X) i wiele innych.

## Krótka historia formatu pliku ZIP

Historia formatu plików ZIP sięga pozwu wytoczonego przez firmę System Enhancement Associates (SEA) przeciwko PKWARE za korzystanie z narzędzia ARC bez pozwolenia na jego znak towarowy oraz prawa autorskie do wyglądu produktu i interfejsu użytkownika. Wcześniej Phil Katz przepisał kod źródłowy SEA i wypuścił PKXARC, ekstraktor ARC i PKARC, kompresor plików, jako darmowe oprogramowanie dla systemów opartych na MS-DOS. Przegrywając w procesie, PKWARE nie mógł już używać niczego związanego z ARC. W tym miejscu powstało nowe narzędzie do kompresji plików, nazwane ZIP, które stało się częścią narzędzia PKZIP firmy PKWARE, Inc.

Katz udostępnił specyfikacje formatu plików ZIP do domeny publicznej, zachowując jednocześnie prawa własności do swojego narzędzia do kompresji i ekstrakcji, tj. PKZIP. System kompresji ZIP był (i jest) w stanie archiwizować pliki w folderze za pomocą 32-bitowego algorytmu cyklicznej kontroli redundancji ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) do kompresji pliku rozmiary. W przeciwieństwie do ARC, foldery .ZIP zawierały plik katalogu, który pełnił rolę książki kodów kryptografa, przechowując informacje niezbędne do renderowania skompresowanych plików.

## Obsługiwane metody kompresji w ZIP

Zgodnie ze specyfikacją formatu pliku .ZIP obsługiwane są następujące metody kompresji.

* Store — oznacza brak kompresji
* Kurczyć
* Redukcja (oznacza to współczynniki kompresji od poziomu 1 do poziomu 4)
* Imploduj
* Siadać
* Deflat64
* BZIP2
* LZMA (EFS)
* WavPack
* PPMd wersja I, Rev 1

DEFLATE to powszechnie stosowana metoda kompresji, która jest algorytmem bezstratnej kompresji danych, który wykorzystuje kombinację kodowania LZ77 i Huffmana i jest szczegółowo opisana w [RFC 1951](https://tools.ietf.org/html/rfc1951).

## Specyfikacje formatu plików ZIP

Pliki ZIP mają możliwość przechowywania wielu plików przy użyciu różnych technik kompresji, a jednocześnie obsługują przechowywanie pliku bez żadnej kompresji. Każdy plik jest przechowywany/kompresowany indywidualnie, co pomaga je rozpakować lub dodać nowe bez stosowania kompresji lub dekompresji do całego archiwum.

### Ogólny format pliku ZIP

Każdy plik ZIP ma następującą strukturę:


|ZIP Format pliku
---|
|Nagłówek pliku lokalnego 1
|Dane pliku 1
|Deskryptor danych 1
|Nagłówek pliku lokalnego 2
|Dane pliku 2
|Deskryptor danych 2
| ....
| ....
|Lokalny nagłówek pliku N
|Dane pliku N
|Deskryptor danych N
|Nagłówek odszyfrowywania archiwum
|Archiwizuj dodatkowy rekord danych
|Centralny katalog

Format pliku ZIP wykorzystuje 32-bitowy algorytm CRC do celów archiwizacji. Aby renderować skompresowane pliki, archiwum ZIP zawiera na końcu katalog, w którym przechowywane są wpisy zawartych plików i ich lokalizacja w pliku archiwum. Pełni zatem rolę kodowania do enkapsulacji informacji niezbędnych do renderowania skompresowanych plików. Czytniki ZIP używają katalogu do załadowania listy plików bez czytania całego archiwum ZIP. Format zachowuje podwójne kopie struktury katalogów, aby zapewnić lepszą ochronę przed utratą danych.

Każdy plik w archiwum ZIP jest reprezentowany jako osobny wpis, gdzie każdy wpis składa się z nagłówka pliku lokalnego, po którym następują dane skompresowanego pliku. Katalog na końcu archiwum zawiera odniesienia do wszystkich tych wpisów plików. Czytniki plików ZIP powinny unikać czytania lokalnych nagłówków plików, a wszelkiego rodzaju listy plików powinny być odczytywane z katalogu. Ten katalog jest jedynym źródłem prawidłowych wpisów plików w archiwum, ponieważ pliki mogą być również dołączane na końcu archiwum. Dlatego jeśli czytnik odczytuje lokalne nagłówki archiwum ZIP od początku, może odczytać również wpisy nieprawidłowe (usunięte) oraz te, które nie są częścią usuwanego z archiwum katalogu.

Kolejność wpisów plików w katalogu centralnym nie musi pokrywać się z porządkiem wpisów plików w archiwum.

### Wpisy plików ZIP

Wpisy w pliku ZIP są ułożone jeden po drugim, gdzie każdy wpis składa się z:

* Lokalny nagłówek pliku
* Opcjonalne dodatkowe pola danych
* Dane użytkownika (opcjonalnie skompresowane/opcjonalnie zaszyfrowane)

Lokalny nagłówek pliku każdego wpisu zawiera informacje o pliku, takie jak komentarz, rozmiar pliku i nazwa pliku. Dodatkowe pola danych (opcjonalnie) mogą pomieścić informacje o opcjach rozszerzania formatu ZIP.

#### Lokalny nagłówek pliku

Lokalny nagłówek pliku ma specyficzną strukturę pól składającą się z wartości wielobajtowych. Wszystkie wartości są przechowywane w kolejności bajtów typu little-endian, gdzie długość pola liczy długość w bajtach. Wszystkie struktury w pliku ZIP używają 4-bajtowych podpisów dla każdego wpisu pliku. Koniec sygnatury katalogu centralnego to 0x06054b50 i można go odróżnić za pomocą własnego unikalnego podpisu. Poniżej przedstawiono kolejność informacji przechowywanych w nagłówku pliku lokalnego.


|Przesunięcie|Bajty|Opis
---|---|---|
|0|4|Podpis nagłówka pliku lokalnego # 0x04034b50 (odczytywany jako liczba little-endian)
|4|2|Wersja potrzebna do wyodrębnienia (minimum)
|6|2|Flaga bitowa ogólnego przeznaczenia
|8|2|Metoda kompresji
|10|2|Czas ostatniej modyfikacji pliku
|12|2|Data ostatniej modyfikacji pliku
|14|4|CRC-32
|18|4|Rozmiar skompresowany
|22|4|Rozmiar nieskompresowany
|26|2|Długość nazwy pliku (n)
|28|2|Dodatkowa długość pola (m)
|30|n|Nazwa pliku
|30+n|m|Dodatkowe pole

#### Nagłówek pliku katalogu centralnego


|Przesunięcie|Bajty|Opis
---|---|---|
|0|4|Podpis nagłówka pliku katalogu centralnego # 0x02014b50
|4|2|Wersja wykonana przez
|6|2|Wersja potrzebna do wyodrębnienia (minimum)
|8|2|Flaga bitowa ogólnego przeznaczenia
|10|2|Metoda kompresji
|12|2|Czas ostatniej modyfikacji pliku
|14|2|Data ostatniej modyfikacji pliku
|16|4|CRC-32
|20|4|Rozmiar skompresowany
|24|4|Rozmiar nieskompresowany
|28|2|Długość nazwy pliku (n)
|30|2|Dodatkowa długość pola (m)
|32|2|Długość komentarza do pliku (k)
|34|2|Numer dysku, na którym rozpoczyna się plik
|36|2|Wewnętrzne atrybuty plików
|38|4|Atrybuty plików zewnętrznych
|42|4|Względne przesunięcie lokalnego nagłówka pliku. Jest to liczba bajtów między początkiem pierwszego dysku, na którym znajduje się plik, a początkiem lokalnego nagłówka pliku. Dzięki temu oprogramowanie odczytujące katalog centralny może zlokalizować pozycję pliku w pliku ZIP.
|46|n|Nazwa pliku
|46+n|m|Dodatkowe pole
|46+n+m|k|Dodaj komentarz

#### Koniec rekordu w centralnej książce telefonicznej


|Przesunięcie|Bajty|Opis
---|---|---|
|0|4|Koniec sygnatury katalogu centralnego # 0x06054b50
|4|2|Numer tego dysku
|6|2|Dysk, na którym zaczyna się katalog centralny
|8|2|Liczba rekordów katalogu centralnego na tym dysku
|10|2|Całkowita liczba rekordów katalogu centralnego
|12|4|Rozmiar katalogu centralnego (bajty)
|16|4|Przesunięcie początku katalogu centralnego względem początku archiwum
|20|2|Długość komentarza (n)
|22|n|Komentarz

## Bibliografia

* [Specyfikacje formatu pliku PKWARE ZIP](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Struktura pliku PKZip](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)

