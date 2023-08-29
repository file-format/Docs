{
  "date" : "2021-08-09",
  "keywords" :[ "plik cso", "format pliku cso", "co to jest plik cso", "plik", "przykład cso", "rozszerzenie pliku cso", "rozszerzenie", "format", "iso", "kompresja DAX " ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Poznaj format pliku CSO i interfejsy API, które mogą tworzyć i otwierać pliki CSO.",
  "title" :"CSO - skompresowany obraz dysku ISO",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## Czym jest plik CSO?

Plik z rozszerzeniem .cso to skompresowany plik obrazu ISO. CSO jest alternatywą dla metody kompresji DAX; znany również jako CISO; była pierwszą metodą kompresji plików [ISO](/pl/compression/iso/) i zwykle jest preferowaną metodą archiwizacji materiałów z PlayStation Portable. Ten format wykorzystuje kompresję Deflate, która może zawierać do dziewięciu warstw kompresji. Do tworzenia obrazów używane jest oprogramowanie takie jak Prometheus i YACC.

## Format pliku CSO

Format pliku CSO był pierwszą metodą kompresji dla ISO w celu zaoszczędzenia większej ilości pamięci. Od czasu do czasu wprowadzano ulepszenia w celu uzyskania lepszej kompresji. CSO używa kompresji Deflate z dziewięcioma poziomami ustawień wstępnych, zwykle każdy poziom może obsłużyć indywidualnie 2 bloki KiB. Podczas gdy najwyższe poziomy kompresji mogą spowolnić i wydłużyć czas ładowania oprogramowania, które w dużej mierze zależy od strumieniowego przesyłania danych z płyt, również niższe poziomy mogą zapewnić znaczną kompresję.

### Struktura plików CSO

Format pliku CSO zawiera 24-bajtowy nagłówek, bloki danych i tabelę indeksów. Little-endian jest przyjmowany dla pól większych niż bajt. Poniżej podano endianowość architektury PlayStation Portable.

#### Nagłówek

| Przesunięcie (bajty) | Imię | Rozmiar (bajty) | Cel |
----------|----------|--------------|---------|
| 0x0 | Magia | 4 | Zawsze CISO lub 0x4F534943 odczytywane jako 32-bitowa liczba całkowita. To pole służy do identyfikacji pliku CSO. Zauważ, że to pole może być inne dla innych pochodnych CSO, np. ZSO używało magicznego kodu ZISO. |
| 0x4 | Rozmiar nagłówka | 4 | W przypadku oryginalnego formatu pliku CSO „v1” to pole jest ignorowane i dlatego nie musi być dokładne. Jednak format „v2” i ZSO wymagają, aby to pole zawsze miało wartość 0x18 (24 bajty). |
| 0x8 | Rozmiar nieskompresowany | 8 | Rozmiar oryginalnego nieskompresowanego ISO w bajtach. |
| 0x10 | Rozmiar bloku | 4 | Rozmiar każdego bloku danych w bajtach przed kompresją. Zwykle 2048 bajtów, tyle samo co rozmiar każdego sektora ISO 9660. |
| 0x14 | Wersja | 1 | Wersja używanego formatu pliku. W przypadku formatu „v1” wartość może wynosić 0 lub 1. W przypadku formatu „v2” musi to być 2. Dodatkowo format ZSO wymaga wartości 1. |
| 0x15 | Wyrównanie indeksu | 1 | Wyrównanie każdego wpisu indeksu, określone w bitach. |
| 0x16 | Zarezerwowane | 2 | To pole jest nieużywane. W formacie „v1” to pole jest ignorowane i może zawierać dowolne wartości. W formacie „v2” to pole musi mieć wartość zero. |

#### Tabela indeksu

Tablica indeksów zawiera kilka 4-bajtowych wpisów, które wskazują pozycję każdego bloku danych oraz dodatkowy, ostatni wpis, który wskazuje na koniec pliku.
Treść każdego wpisu jest następująca:
| Kawałek | Długość | Maska | Imię | Cel |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFFF | Pozycja | To pole, przesunięte w lewo o wyrównanie indeksu podane w nagłówku, podaje pozycję, w której zaczyna się blok danych. |
| 31 | 1 | 0x80000000 | Rodzaj kompresji | Format ZSO ma podobną semantykę, tyle że 0 reprezentuje LZ4 zamiast Deflate. W formacie „v2”. Blok jest niejawnie uważany za nieskompresowany, jeśli rozmiar bloku jest równy lub większy niż rozmiar bloku określony w nagłówku pliku. |

#### Bloki danych

Bloki danych składają się z nieskompresowanych lub skompresowanych danych. Rozmiar bloku oblicza się, pobierając jego pozycję, a następnie odejmując ją od pozycji następnego bloku. Jeśli wyrównanie indeksu jest większe od zera, prawdopodobnie rozmiar bloku jest większy niż przechowywane w nim dane.


## Bibliografia

* N/A

