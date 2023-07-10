{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST — format pliku pamięci programu Outlook",
  "description":"Poznaj format plików OST i interfejsy API, które mogą tworzyć i otwierać pliki OST.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest plik OST?

Pliki OST lub Offline Storage reprezentują dane skrzynki pocztowej użytkownika w trybie offline na komputerze lokalnym po rejestracji na serwerze Exchange przy użyciu programu Microsoft Outlook. Jest tworzony automatycznie przy pierwszym użyciu programu Microsoft Outlook po nawiązaniu połączenia z serwerem. Po utworzeniu pliku dane są synchronizowane z serwerem pocztowym, dzięki czemu są dostępne również w trybie offline w przypadku rozłączenia z serwerem pocztowym. Pliki OST mogą zawierać elementy skrzynki pocztowej użytkownika, takie jak e-maile, kontakty, informacje z kalendarza, notatki, zadania i inne podobne dane. Użytkownicy mogą tworzyć wiadomości e-mail i inne elementy danych w pliku OST nawet w przypadku braku połączenia z serwerem, ale nie będą one synchronizowane z serwerem. Po nawiązaniu połączenia plik lokalny jest ponownie synchronizowany z serwerem, dzięki czemu zarówno serwer, jak i kopia lokalna mają ten sam poziom informacji.

## Format pliku OST

Format plików OST (Offline Storage Table) i [PST](/pl/email/pst/) (Personal Storage Table) składa się z formatu pliku folderów osobistych (PFF), który odpowiada przechowywaniu wiadomości e-mail, kontaktów i spotkań użytkownika. Dane w pliku PFF są przechowywane w little-endian, a wszystkie daty i godziny są reprezentowane jako FILETIME w UTC. [MS-PST] definiuje dwa typy PFF:

* 32-bitowy format ANSI
* 64-bitowy format Unicode

Format pliku PST [specyfikacje](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), udostępniony przez firmę Microsoft, ma również zastosowanie do formatu pliku OST jako bezpłatny i nieodwołalne licencjonowanie patentów w ramach Obietnicy Otwartej Specyfikacji. Składa się z następujących wyróżniających się elementów:

* Uciekaj nagłówek
* Dane nagłówka pliku
* Węzeł gałęzi indeksu
* Węzeł liścia indeksu
* (Plik) indeks przesunięcia
* (Pozycja) indeks deskryptora
* Lokalne deskryptory
* Typ tabeli pozycji

### Informacje nagłówka

Struktura HEADER pliku OST znajduje się na samym początku pliku z przesunięciem 0. Zawiera metadane dotyczące pliku OST i informacje ROOT umożliwiające dostęp do opisanych powyżej struktur danych warstwy NDB. Struktura HEADER różni się dla wersji Unicode i ANSI formatu plików OST.

Nagłówek zaczyna się od 4-bajtowego magicznego słowa **!BDN** reprezentowanego przez bajty (0x21, 0x42, 0x44, 0x4E). Kolejna 2-bajtowa magiczna liczba, **SM** (0x53, 0x4D), znajduje się na przesunięciu 8 od początku pliku. Informacje o wersji (ANSI lub Unicode) są przesunięte o 10 od początku pliku. Wartość szesnastkowa (0x17) określa plik Unicode OST, podczas gdy 0x0E lub 0x0F reprezentuje format pliku ANSI.

|Pole|Opis
---|---|
|dwMagic (4 bajty)|MUSI być "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 bajty)|32-bitowa wartość CRC 471 bajtów danych, począwszy od wMagicClient (0ffset 0x0008)
|wMagicClient (2 bajty)|MUSI mieć wartość „{ 0x53, 0x4D }”.
|wVer (2 bajty)|Wersja formatu pliku. Ta wartość MUSI wynosić 14 lub 15, jeśli plik jest plikiem ANSI PST, i MUSI wynosić 23, jeśli plik jest plikiem PST Unicode.
|wVerClient (2 bajty)|Wersja formatu pliku klienta. Wersja odpowiadająca formatowi opisanemu w tym dokumencie to 19. Twórcy nowego pliku PST opartego na tym dokumencie POWINNI zainicjować tę wartość na 19.
|bPlatformCreate (1 bajt)|Ta wartość MUSI być ustawiona na 0x01.
|bPlatformAccess (1 bajt)|Ta wartość MUSI być ustawiona na 0x01.
|dwReserved (8 bajtów)|
|bidUnused (tylko 8 bajtów Unicode)|Nieużywane wypełnienie dodane podczas tworzenia formatu pliku PST Unicode.
|bidNextP (Unicode: 8 bajtów; ANSI: 4 bajty)|Następna strona BID. Strony mają specjalny licznik do przydzielania wartości bidIndex. Z tego licznika przydzielana jest wartość bidIndex dla BID-ów dla stron.
|bidNextB (tylko 4 bajty ANSI): |Następny BID. Ta wartość jest licznikiem monotonicznym, który wskazuje BID do przypisania dla następnego przydzielonego bloku. Wartości BID zwiększają się o 4. Więcej informacji znajduje się w sekcji 2.2.2.2.
|dwUnique (4 bajty)|Jest to monotonicznie rosnąca wartość, która jest modyfikowana za każdym razem, gdy modyfikowana jest struktura HEADER pliku PST. Funkcją tej wartości jest zapewnienie unikalnej wartości i zapewnienie, że CRC HEADER będą różne po każdej modyfikacji nagłówka.
|rgnid[](128 bajtów)|Stała tablica 32 identyfikatorów NID, z których każdy odpowiada jednemu z 32 możliwych typów NID_TYPE (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_TYPE_ASSOC_MESSAGE)
|qwNiewykorzystane (8 bajtów)|Niewykorzystane miejsce; MUSI być ustawiony na zero. Tylko format pliku PST Unicode.
|root (Unicode: 72 bajty; ANSI: 40 bajtów)|Struktura ROOT (sekcja 2.2.2.5).
|dwAlign (4 bajty)|Niewykorzystane bajty wyrównania; MUSI być ustawiony na zero. Tylko format pliku PST Unicode.
|rgbFM (128 bajtów)|Przestarzały FMap. To nie jest już używane i MUSI być wypełnione 0xFF. Czytelnicy POWINNI ignorować wartość tych bajtów.
|rgbFP (128 bajtów)|Przestarzała mapa FP. To nie jest już używane i MUSI być wypełnione 0xFF. Czytelnicy POWINNI ignorować wartość tych bajtów.
|bSentinel (1 bajt)|MUSI być ustawiony na 0x80.
|bCryptMethod (1 bajt)|Wskazuje sposób kodowania danych w pliku PST. MUSI być ustawiona na jedną z predefiniowanych wartości (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbZarezerwowane (2 bajty)| Skryty; MUSI być ustawiony na zero.
|bidNextB (8 bajtów)|Wskazuje następną dostępną wartość BID. Tylko format pliku PST Unicode.
|bidNextB (TYLKO Unicode: 8 bajtów)|Następna BID. Ta wartość jest licznikiem monotonicznym, który wskazuje BID do przypisania dla następnego przydzielonego bloku. Wartości BID zwiększają się o 4. Więcej informacji znajduje się w sekcji 2.2.2.2.
|dwCRCFull (4 bajty)|32-bitowa wartość CRC 516 bajtów danych, począwszy od wMagicClient do bidNextB włącznie. Tylko format pliku PST Unicode.
|ullZarezerwowany (8 bajtów)|Zarezerwowany; MUSI być ustawiony na zero. Tylko format pliku ANSI PST.
|dwZarezerwowane (4 bajty)|Zarezerwowane; MUSI być ustawiony na zero. Tylko format pliku ANSI PST.
|rgbReserved2 (3 bajty)|
|bZarezerwowane (1 bajt) |
|rgbReserved3 (32 bajty) |

## Bibliografia

* [Format pliku folderów osobistych programu Outlook (.ost)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Specyfikacje formatu plików folderów osobistych](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

