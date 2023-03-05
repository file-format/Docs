{
  "date" : "2021-04-08",
  "keywords" :["plik lz4", "format pliku lz4", "co to jest plik lz4", "plik", "przykład lz4", "rozszerzenie pliku lz4", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku skompresowanego LZ4 - LZ4",
  "description":"Poznaj format pliku LBR i interfejsy API, które mogą tworzyć i otwierać pliki LZ4.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Czym jest plik LZ4?

Plik z rozszerzeniem .lz4 to skompresowany plik archiwum utworzony za pomocą aplikacji/narzędzi obsługujących kompresję [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)). Algorytm LZ4 koncentruje się na kompromisie między szybkością a współczynnikiem kompresji. Skompresowane archiwa LZ4 można tworzyć za pomocą narzędzia wiersza poleceń LZ4 i dekompresować za pomocą tego samego narzędzia.

## Format pliku LZ4

Format pliku LZ4, oparty na algorytmie kompresji LZ4, jest niezależny od typu procesora, systemu operacyjnego, systemu plików i zestawu znaków. Nadaje się do kompresji plików i kompresji strumieniowej przy użyciu algorytmu LZ4. Wstępna implementacja formatu LZ4 została przeprowadzona w języku [C](/pl/programming/c/) przez Yanna Colleta w 2011 roku i jest dostępna do wglądu dla programistów na [Github](https://github.com/lz4/lz4) .

### Format ramki LZ4

Ogólna struktura formatu pliku LZ4 jest pokazana poniżej.

|MagiaNb|F. deskryptor| Blok|(...)|Znacznik końca |C. suma kontrolna|
---|---|---|---|---|---|
|4 bajty| 3-15 bajtów||| 4 bajty| 0-4 bajtów|

#### Magiczny numer

4 bajty, format Little Endian. Wartość : 0x184D2204

#### Deskryptor ramki

Deskryptor ramki składa się z 3 do 15 bajtów i jest najważniejszą częścią specyfikacji. Razem pola Magic_Number i Frame_Descriptor są określane jako nagłówek ramki LZ4, a ich rozmiar waha się od 7 do 19 bajtów. Jest tak, jak pokazano poniżej.

|FLG| BD| (Rozmiar zawartości)| (identyfikator słownika)| HC|
---|---|---|---|---|
|1 bajt| 1 bajt| 0 - 8 bajtów| 0 - 4 bajty| 1 bajt|

#### Bloki danych

Każdy blok danych ma następującą kolejność.

|Rozmiar bloku| dane| (Suma kontrolna bloku)|
---|---|---|
|4 bajty| |0 - 4 bajty|

#### Znak końca

Przepływ bloków kończy się, gdy po ostatnim bloku danych następuje 32-bitowa wartość 0x00000000.

#### Suma kontrolna zawartości

Content_Checksum weryfikuje poprawność dekodowania treści i jest przeprowadzany z wykorzystaniem wyniku algorytmu xxHash-32. Sprawdza wyniki pomyślnej transmisji wszystkich bloków we właściwej kolejności i bez żadnych błędów.

## Bibliografia

* [Format ramki LZ4](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [Algorytm kompresji LZ4 – Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

