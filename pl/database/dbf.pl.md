{
  "date" : "2021-06-15",
  "keywords" :["DBF", "rozszerzenie", "plik dbf", "format pliku dbf", "Typ pliku bazy danych", "Format pliku bazy danych", "co to jest plik dbf", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku DBF i interfejsy API, które mogą tworzyć i otwierać pliki DBF.",
  "title" :"DBF - Plik Bazy Danych dBase",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## Czym jest plik DBF?
Plik z rozszerzeniem .dbf jest plikiem bazy danych używanym przez aplikację systemu zarządzania bazami danych o nazwie **dBASE**. Początkowo baza danych dBASE nosiła nazwę Project Vulcan; rozpoczęty przez **Wayne'a Ratliffa** w 1978 roku. Typ pliku DBF został wprowadzony w dBASE II w 1983 roku. Organizuje on wiele rekordów danych z polami typu Array. Oprogramowanie bazy danych **xBase**, które jest popularne ze względu na kompatybilność z szeroką gamą formatów plików; obsługuje również pliki DBF.

## Format pliku DBF
Format pliku DBF należy do systemu zarządzania bazą danych dBASE, ale może być kompatybilny z xBase lub innym oprogramowaniem DBMS. Początkowa wersja pliku dbf składała się z prostej tabeli, w której można było dodawać, modyfikować, usuwać lub drukować dane przy użyciu zestawu znaków ASCII. Z biegiem czasu .dbf był ulepszany i dodawano dodatkowe pliki zwiększające funkcjonalność i możliwości systemu bazodanowego.

We współczesnym dBASE plik DBF składa się z nagłówka, rekordów danych i znacznika EOF (End of File)

- W nagłówku znajdują się informacje o pliku, takie jak liczba rekordów oraz liczba typów pól użytych w rekordach.
- Zapisy zawierają rzeczywiste dane.
- Koniec pliku jest oznaczony pojedynczym bajtem o wartości 0x1A.

### Nagłówek pliku
Układ nagłówka pliku w dBase przedstawia poniższa tabela:

| Bajt | Spis treści | Znaczenie |
---|---|---|
| 0 | 1 bajt | Prawidłowy dBASE dla pliku DOS; bity 0–2 wskazują numer wersji, bit 3 wskazuje na obecność pliku memo dBASE dla DOS, bity 4–6 wskazują na obecność tabeli SQL, bit 7 wskazuje na obecność dowolnego pliku memo (dBASE m PLUS lub dBASE dla DOS) |
| 1–3 | 3 bajty | Data ostatniej aktualizacji; sformatowany jako RRMMDD |
| 4–7 | liczba 32-bitowa | Liczba rekordów w zbiorze bazy danych |
| 8–9 | liczba 16-bitowa | Liczba bajtów w nagłówku |
| 10–11 | liczba 16-bitowa | Liczba bajtów w rekordzie |
| 12–13 | 2 bajty | Skryty; wypełnij 0 |
| 14 | 1 bajt | Oznaczenie wskazujące na niezakończoną transakcję[uwaga 1] |
| 15 | 1 bajt | Flaga szyfrowania [uwaga 2] |
| 16–27 | 12 bajtów | Zarezerwowane dla dBASE dla DOS w środowisku wielu użytkowników |
| 28 | 1 bajt | Flaga produkcyjnego pliku .mdx; 1 jeśli istnieje produkcyjny plik .mdx, 0 jeśli nie |
| 29 | 1 bajt | Identyfikator sterownika językowego |
| 30–31 | 2 bajty | Skryty; wypełnij 0 |
| 32–n [przypis 3][przypis 4] | 32 bajty każdy | tablica deskryptorów pól (patrz poniżej układ deskryptorów) |
| n + 1 | 1 bajt | 0x0D jako terminator tablicy deskryptorów pól |

- Funkcja ISMARKEDO sprawdza tę flagę (BEGIN TRANSACTION ustawia ją na 1, END TRANSACTION i ROLLBACK resetują ją do 0).
- Jeśli ta flaga jest ustawiona na 1, pojawia się komunikat Baza danych zaszyfrowana.
- Maksymalna liczba pól to 255.
- n oznacza ostatni bajt w tablicy deskryptorów pól.

### Tablica deskryptorów pól
Układ deskryptorów pól w dBASE:

| Bajt | Spis treści | Znaczenie |
---|---|---|
| 0–10 | 11 bajtów | Nazwa pola w ASCII (wypełniona zerami) |
| 11 | 1 bajt | Typ pola. Dozwolone wartości: C, D, F, L, M lub N (znaczenia w następnej tabeli) |
| 12–15 | 4 bajty | Zarezerwowane |
| 16 | 1 bajt | Długość pola w formacie binarnym (maksymalnie 254 (0xFE)). |
| 17 | 1 bajt | Liczba dziesiętna pola w systemie binarnym |
| 18–19 | 2 bajty | Identyfikator obszaru roboczego |
| 20 | 1 bajt | Przykład |
| 21–30 | 10 bajtów | Zarezerwowane |
| 31 | 1 bajt | Flaga pola produkcyjnego MDX; 1 jeśli pole ma znacznik indeksu w produkcyjnym pliku MDX, 0 jeśli nie |

### Rekordy bazy danych
Każdy rekord zaczyna się od flagi usunięcia (1-bajtowej). Pola są pakowane w rekordy bez separatorów pól. Wszystkie dane pola są w formacie ASCII. W zależności od rodzaju pola aplikacja nakłada dodatkowe ograniczenia. Oto typy pól w dBase:

| Typ pola | Mnemonik | Co akceptuje |
-------|-----|----|
| C | znak | Dowolny tekst ASCII (dopełniony spacjami do długości pola) |
| D | Data | Cyfry i znak oddzielający miesiąc, dzień i rok (przechowywane wewnętrznie jako 8 cyfr w formacie RRRRMMDD) |
| F. | Zmiennoprzecinkowy | -, ., 0–9 (wyrównanie do prawej, wypełnione spacjami) |
| L | logiczne | Y, y, N, n, T, t, F, f lub ? (gdy niezainicjowany) |
| M | Notatka | Dowolny tekst ASCII (przechowywany wewnętrznie jako 10 cyfr reprezentujących numer bloku .dbt, wyrównany do prawej, uzupełniony spacjami) |
| N | Numeryczne | -, ., 0–9 (wyrównanie do prawej, wypełnione spacjami) |









## Bibliografia ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)

