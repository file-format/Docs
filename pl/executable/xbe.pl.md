{
  "date" : "2021-08-31",
  "keywords" :["plik xbe", "format pliku xbe", "co to jest plik xbe", "plik", "przykład xbe", "rozszerzenie pliku xbe", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format plików XBE i interfejsy API, które mogą tworzyć i otwierać pliki XBE.",
  "title" :"XBE - plik pakietu aplikacji iOS",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## Czym jest plik XBE?
Plik z rozszerzeniem .xbe to wykonywalna aplikacja z dysku z grą wideo Xbox. Pliki XBE to główne pliki, które są wykonywane w systemie Xbox i nie powinny być otwierane typowo na komputerze, ale można je otworzyć na komputerze PC za pomocą programu do emulacji Xbox. Pliki te są zwykle tworzone przez twórców gier, a następnie podpisywane przez firmę Microsoft. Struktura plików jest podobna do plików Windows PE, ale zastosowano kilka ważnych zmian zgodnie z ustawieniami XBox, aby można je było uruchamiać na XBox.

## Format pliku XBE
Plik XBE składa się z nagłówka obrazu, zbioru nagłówków sekcji, certyfikatu, danych lokalnego magazynu wątków, zbioru wersji bibliotek, bitmapy firmy Microsoft oraz sekcji zawierających kod i zasoby.

### Nagłówek obrazu
Nagłówek obrazu zawiera informacje wyjaśniające, gdzie w pliku znajdują się inne komponenty pliku wykonywalnego oraz w jaki sposób plik wykonywalny powinien być traktowany i ładowany.

### Tabela TLS
Tabela TLS zawiera wszystkie informacje potrzebne XBE do prawidłowego skonfigurowania lokalnej pamięci masowej wątków. Jest zasadniczo unikalny dla katalogu TLS znajdującego się w plikach PE32 i można go stamtąd bezpośrednio skopiować. Tę tabelę można pominąć, jeśli plik XBE nie korzysta z pamięci lokalnej wątków, a odpowiednie pole w nagłówku obrazu jest ustawione na zero.

| Przesunięcie | Rozmiar | Imię | Opis |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Surowe dane Początek | Bezwzględny (tj. nie RVA) adres początku danych zmiennej TLS w obrazie programu. |
| 0x0004 | 0x0004 | Surowe dane Koniec | Bezwzględny (tj. nie RVA) adres końca danych zmiennej TLS w obrazie programu. |
| 0x0008 | 0x0004 | Adres indeksu | Bezwzględny (tj. nie RVA) adres zmiennej indeksu TLS. |
| 0x000C | 0x0004 | Adres wywołań zwrotnych | Adres bezwzględny (tj. nie RVA) tabeli funkcji wywołania zwrotnego TLS zakończonej znakiem null. |
| 0x0010 | 0x0004 | Rozmiar wypełnienia zerowego | Liczba bajtów następujących po nieprzetworzonych danych, które powinny być ustawione na zero w pamięci. |
| 0x0014 | 0x0004 | Charakterystyka | Opisuje wyrównanie. |

### Certyfikat

Certyfikat jest obowiązkowy dla każdego pliku wykonywalnego Xbox, który zawiera informacje o tytułach:
 


- Data i godzina utworzenia certyfikatu
- Identyfikator tytułu
- Nazwa tytułu
- Alternatywne identyfikatory tytułów
- Dozwolone typy nośników, z których można uruchomić plik wykonywalny (HD, DVD, CD itp.)
- Region gry
- Oceny gier
- Numer dysku
- Wersja
— Nieprzetworzone dane klucza sieci LAN używane dla łącza systemowego
- Surowe dane klucza podpisu (używane do podpisywania zapisanych gier)
- Alternatywne klucze podpisu
- Oryginalny rozmiar certyfikatu
- Nazwa usługi online (nieobecna we wczesnych plikach wykonywalnych)
- Flagi bezpieczeństwa w czasie wykonywania (nieobecne we wczesnych plikach wykonywalnych)
 


### Dozwolone typy multimediów
Typy nośników, z których plik wykonywalny może być uruchamiany. Znane są następujące wartości:
| Rodzaj nośnika | Wartość |
---------------------|------------|
| TWARDY_DYSK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| płyta | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| KLUCZ | 0x00000100 |
| MEDIA_TABLICA | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MASKA_MEDIA | 0x00FFFFFF |

### Sekcje
Sekcje są wyrażone przez nagłówki sekcji. Nagłówki sekcji rozpoczynają się zaraz po certyfikacie i zawierają informacje, gdzie w pliku faktycznie znajdują się sekcje. W pliku wykonywalnym Xbox zawsze znajdują się co najmniej dwie sekcje:


- .tekst


- .rdata


## Bibliografia



* [Xbe — plik wykonywalny XBox](https://xboxdevwiki.net/Xbe)


