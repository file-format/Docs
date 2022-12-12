{
  "date" : "2021-09-08",
  "keywords" :["plik rel", "format pliku rel", "co to jest plik rel", "plik", "przykład rel", "rozszerzenie pliku rel", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku REL i interfejsy API, które mogą tworzyć i otwierać pliki REL.",
  "title" :"REL - Przenośny Plik Modułu",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Czym jest plik REL?
Plik z rozszerzeniem .rel może być używany do kilku rodzajów celów. Dlatego pod względem klasyfikacji gier jest znany jako relokowalny plik modułu używany przez niektóre gry Nintendo Wii, takie jak Brawl, Super Smash Bros i Mario Kart Wii. Zawiera dane rozgrywki, w tym modele postaci i etapy. Pliki REL działają podobnie do plików .DLL używanych przez system Microsoft Windows.

## Format pliku REL
W formacie pliku REL plik jest podzielony na kilka sekcji, pogrupowanych według podobnego dostępu, np. dane tylko do odczytu w jednej sekcji, cały kod wykonywalny jest umieszczony w innej, itp. Plik rozpoczyna się sekcją nagłówka, po której następuje:
- Tabela zawierająca informacje o sekcji.
- Dane sekcji.
- Informacje o przeprowadzce.

### Nagłówek pliku
Plik zaczyna się od nagłówka o długości do 0x4C bajtów:
| Przesunięcie | Rozmiar | Nazwa pola | Opis |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | identyfikator | Dowolny numer identyfikacyjny. Musi być unikalny wśród wszystkich REL używanych przez grę. Nie może wynosić 0. |
| 0x04 | 4 | następny | Wskaźnik do następnego modułu, wypełniany w czasie wykonywania. |
| 0x08 | 4 | poprzedni | Wskaźnik do poprzedniego modułu, wypełniany w czasie wykonywania. |
| 0x0c | 4 | liczbaSekcje | Liczba sekcji w pliku. |
| 0x10 | 4 | przekrójInformacjePrzesunięcie | Odsunięcie do początku tabeli przekroju. |
| 0x14 | 4 | nazwaPrzesunięcie | Przesunięcie do ciągu ASCII zawierającego nazwę modułu. Może być NULL. Względem początku pliku REL. |
| 0x18 | 4 | nazwaRozmiar | Rozmiar nazwy modułu w bajtach. |
| 0x1c | 4 | wersja | Numer wersji formatu pliku REL. |
| 0x20 | 4 | bssRozmiar | Rozmiar sekcji „.bss”. |
| 0x24 | 4 | odsunięcie względne | Przesunięcie do tabeli relokacji. |
| 0x28 | 4 | impPrzesunięcie | Przesunięcie do tabeli imp. |
| 0x2c | 4 | impRozmiar | Rozmiar tabeli imp w bajtach. |
| 0x30 | 1 | prologSekcja | Indeks do tabeli sekcji, do której odnosi się prolog. Pomiń, jeśli to pole ma wartość 0. |
| 0x31 | 1 | epilogSekcja | Indeks do tabeli sekcji, do której odnosi się epilog. Pomiń, jeśli to pole ma wartość 0. |
| 0x32 | 1 | nierozwiązanySekcja | Indeks do tabeli sekcji, do której odnosi się nierozwiązany. Pomiń, jeśli to pole ma wartość 0. |
| 0x33 | 1 | bssSekcja | Indeks do tabeli sekcji, do której odnosi się bss. Wypełniony w czasie wykonywania! |
| 0x34 | 4 | prolog | Przesunięcie do określonej sekcji funkcji _prolog. |
| 0x38 | 4 | epilog | Przesunięcie do określonej sekcji funkcji _epilog. |
| 0x3c | 4 | nierozwiązany | Przesunięcie do określonej sekcji funkcji _unresolved. |
| 0x40 | 4 | wyrównać | Tylko wersja ≥ 2. Wiązanie wyrównania dla wszystkich sekcji, wyrażone jako potęga 2. |
| 0x44 | 4 | bssWyrównaj | Tylko wersja ≥ 2. Ograniczenie wyrównania dla wszystkich sekcji „.bss”, wyrażone jako potęga 2. |
| 0x48 | 4 | naprawRozmiar | Tylko wersja ≥ 3. Jeśli REL jest połączony z OSLinkFixed (zamiast OSLink), spacja po tym adresie może być wykorzystana do innych celów (np. BSS). |

### Tabela informacji o sekcji
Tabela informacji o sekcji zawiera wpisy **numSections**, każdy o długości 0x8 bajtów:
| Przesunięcie | Rozmiar | Opis |
-------|------------|-------------|
| 0x0 | 30 bitów | Przesunięcie od początku REL do sekcji. Jeśli jest to zero, sekcja jest sekcją niezainicjowaną (tj. .bss). |
| 0x3.6 | 1 bit | Nieznany. |
| 0x3.7 | 1 bit | Flaga wykonywalna; jeśli jest to 1, sekcja jest wykonywalna. |
| 0x4 | 4 | Długość sekcji w bajtach. Jeśli jest to zero, ten wpis jest pomijany. |
| 0x8 | Następny wpis | Następny wpis |

### Dane relokacji
Dane relokacji to jedna lub więcej list struktur bajtów 0x8. Koniec każdej listy jest oznaczony specjalnym kodem typu 203:
| Przesunięcie | Imię | Rozmiar | Opis |
-------|------------|------------|-----|
| 0x0 | przesunięcie | 2 | Przesunięcie w bajtach od poprzedniej relokacji do tej. Jeśli jest to pierwsza relokacja w sekcji, jest ona względna względem początku sekcji. |
| 0x2 | wpisz | 1 | Typ przeprowadzki. Opisane poniżej. |
| 0x3 | sekcja | 1 | Sekcja symbolu, względem której ma zostać przeniesione. W przypadku specjalnego typu relokacji 202 jest to zamiast tego numer sekcji w tym pliku, do której odnoszą się następujące wpisy relokacji. |
| 0x4 | dodaj | 4 | Przesunięcie w bajtach symbolu, względem którego ma zostać przeniesione, względem początku jego sekcji. Zamiast tego jest to adres bezwzględny dla relokacji względem main.dol. |
| 0x8 | Następny wpis | Następny wpis | Następny wpis |


 




## Bibliografia


* [Relocatable Object Module Format](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


