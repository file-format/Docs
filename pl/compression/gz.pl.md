{
  "date" : "2019-10-11",
  "keywords" :[ "plik gz", "format pliku gz", "co to jest plik gz", "plik", "przykład gz", "rozszerzenie pliku gz", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku GZ - Spakowany plik archiwum GNU",
  "description":"Dowiedz się, co to jest plik GZ i interfejsy API, które mogą tworzyć i otwierać pliki GZ.",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik GZ?

Plik GZ to skompresowane archiwum utworzone przy użyciu standardowego algorytmu kompresji [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Może zawierać wiele skompresowanych plików, katalogów i kodów pośredniczących plików. Format ten został początkowo opracowany w celu zastąpienia formatów kompresji w systemach UNIX. i nadal jest jednym z najpopularniejszych typów archiwów w systemach Linux. Aplikacje takie jak [WinZip](https://www.winzip.com/en/) mogą otwierać pliki GZ, aby przeglądać ich zawartość zarówno w systemie Windows, jak i MacOS.

## Format pliku GZ — więcej informacji

Gzip używa algorytmu [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) do kompresji archiwum i różni się od formatu archiwum [ZIP](/pl/compression/zip/) tym, że stosuje algorytm kompresji do całego archiwum zamiast pojedynczych plików. Specyfikacja formatu pliku GZIP w wersji 4.3 opublikowana przez Internet Engineering Task Force (IETF) zawiera szczegółowe informacje o formacie pliku. Format pliku składa się z:

* Nagłówek pliku
* Opcjonalne nagłówki
* Skompresowane dane
* Stopka pliku

## Nagłówek pliku GZ ##

Nagłówek pliku GZ składa się z 10 bajtów w następujący sposób:

|Przesunięcie|Rozmiar|Wartość|Opis
---|---|---|---|
|0|2|0x1f 0x8b|Magiczna liczba identyfikująca typ pliku
|2|1| |Metoda kompresji * 0-7 (Zarezerwowane) * 8 (Spuścić powietrze)
|3|1| |Flagi plików
|4|4| |32-bitowy znacznik czasu
|8|1| |Flagi kompresji
|9|1| |Identyfikator systemu operacyjnego

### Flagi plików ###

|Wartość|Identyfikator|Opis
---|---|---|
|0x01|FTEXT|Jeśli ustawione, nieskompresowane dane muszą być traktowane jako tekst zamiast danych binarnych. Ta flaga wskazuje konwersję końca wiersza dla międzyplatformowych plików tekstowych, ale jej nie wymusza.
|0x02|FHCRC|Plik zawiera sumę kontrolną nagłówka (CRC-16)
|0x04|FEXTRA|Plik zawiera dodatkowe pola
|0x08|FNAME|Plik zawiera oryginalną nazwę pliku
|0x10|FCOMMENT|Plik zawiera komentarz
|0x20| |Zarezerwowany
|0x40| |Zarezerwowany
|0x80| |Zarezerwowany

### System operacyjny ###

|Wartość|Opis
---|---|
|0|System plików FAT (MS-DOS, OS/2, NT/Win32)
|1|Amigi
|2|VMS (lub OpenVMS)
|3|Uniks
|4|VM/CMS
|5|Atari TOS
|6|System plików HPFS (OS/2, NT)
|7|Macintosh
|8|Układ Z
|9|CP/M
|10|TOPS-20
|11|System plików NTFS (NT)
|12|QDOS
|13|Żołądź RISCOS
|255|nieznane

## Opcjonalne nagłówki GZ ##

Opcjonalne dodatkowe nagłówki są oznaczone flagami plików i zawierają informacje, takie jak oryginalna nazwa pliku, dodatkowe pola, komentarze i suma kontrolna nagłówka.

## Skompresowane dane ##

Ta sekcja zawiera skompresowane dane przy użyciu algorytmu kompresji DEFLATE.

## Stopka pliku GZ ##

Stopka pliku ma rozmiar 8 bajtów i zawiera następujące informacje.

|Przesunięcie|Rozmiar|Opis
---|---|---|
|0|4|Suma kontrolna (CRC-32)
|4|4|Wartość rozmiaru nieskompresowanych danych w bajtach

## Bibliografia ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: specyfikacja formatu pliku GZIP](https://datatracker.ietf.org/doc/html/rfc1952), przez IETF.

