{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST — format pliku magazynu informacji osobistych programu Outlook",
  "description":"Poznaj format pliku PST i interfejsy API, które mogą tworzyć i otwierać pliki PST.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest plik PST?

Pliki z rozszerzeniem .pst reprezentują pliki pamięci masowej programu Outlook (zwane także tabelami pamięci osobistej), które przechowują różne informacje o użytkowniku. Informacje o użytkownikach są przechowywane w folderach różnych typów, które obejmują wiadomości e-mail, pozycje kalendarza, notatki, kontakty i kilka innych formatów plików. Pliki PST służą do archiwizacji danych wysyłanych e-mailem w trybie offline, które można później ładować i przeglądać w różnych aplikacjach.

## Specyfikacje formatu pliku PST

Format pliku PST [specyfikacje](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx) są udostępniane przez firmę Microsoft jako bezpłatne i nieodwołalne bezpłatne licencje patentowe w ramach obietnicy otwartej specyfikacji .

### Typ formatów PST

Formaty plików PST są podzielone na dwa typy w zależności od kodowania typu pliku. Pliki PST zakodowane w standardzie ANSI są starszymi formatami plików i są obsługiwane tylko przez program Outlook 2002 i wcześniejsze wersje. Takie pliki mają maksymalny rozmiar 2 GB (2^^31^^ bajtów) i nie obsługują Unicode. Bardziej nowoczesny typ formatu pliku, oparty na kodowaniu Unicode, usuwa ograniczenie rozmiaru pliku i może osiągnąć maksymalny rozmiar danych 50 GB.

### Logiczna organizacja formatu pliku PST

U podstaw formatu pliku PST leży B-Tree, które utrzymuje sortowanie danych i umożliwia wyszukiwanie, sekwencyjny dostęp, wstawianie, usuwanie itp. w czasie logarytmicznym. Ogólna struktura pliku PST jest zorganizowana w trzech warstwach.

![Logical layers of a PST file](/pl/email/PST-1.png "Logical layers of a PST file")

Warstwa bazy danych węzłów (NDB) — warstwa bazy danych węzłów znajduje się na niższym poziomie pliku PST i zawiera bazę danych węzłów. Te węzły w rzeczywistości reprezentują urządzenia do przechowywania niższego poziomu w formacie pliku PST. Warstwa NDB składa się z nagłówka, informacji o alokacji plików, bloków i BTrees (Node BTree i Block BTree) z punktu widzenia przechowywania. Węzły i bloki warstwy NDB są połączone poprzez Data BID, która jest jedną z czterech właściwości Node reference, tj. NID (Node ID), Parent NID, Data BID (Block BID) i SubNode BID.

`Listy, tabele i warstwa właściwości —` Warstwa LTP zapewnia logiczne zrozumienie koncepcji wyższego poziomu na szczycie NDB. Oprócz innych elementów warstwa LTP składa się głównie z kontekstu właściwości (PC) i kontekstu tabeli (TC). PC to zbiór właściwości, podczas gdy TC reprezentuje dwuwymiarową macierz zbioru właściwości w porównaniu z ich obecnością. Wydajna implementacja komputerów PC i TC, warstwa LTP wykorzystuje następujące dwa typy struktur danych na szczycie węzła NDB:

* Heap On Node (HN) - umożliwia podrzędną alokację strumienia danych węzła na małe fragmenty o zmiennej wielkości.
* BTree on Heap (BTH) - BTH zapewnia wygodny i praktyczny sposób przeszukiwania danych. Opisane powyżej komputery PC są zaimplementowane jako BTH i dlatego są realizowane poprzez budowanie wewnątrz struktury HN.

`Messaging Layer -` W tej warstwie zaimplementowano reguły wyższego poziomu i logikę biznesową do pracy z plikami PST. Logicznym wyjściem tej warstwy są obiekty folderów, obiekty wiadomości, obiekty załączników i właściwości, co jest możliwe dzięki połączeniu warstw LTP i NDB. Na tej warstwie zdefiniowane są również zasady i wymagania, którymi należy się kierować przy modyfikowaniu zawartości PST.

### Fizyczna organizacja formatu pliku PST

Wysoki poziom organizacji plików w pliku PST przedstawia poniższy rysunek. To tylko przegląd różnych koncepcji z logicznych elementów pliku PST.

![Physical organization of the PST file format](/pl/email/PST-2.png "Physical organization of the PST file format")


#### Informacje nagłówka PST

Struktura HEADER pliku PST znajduje się na samym początku pliku z przesunięciem 0. Zawiera metadane dotyczące pliku PST i informacje ROOT umożliwiające dostęp do opisanych powyżej struktur danych warstwy NDB. Struktura HEADER różni się dla wersji Unicode i ANSI formatu pliku PST.

Nagłówek zaczyna się od 4-bajtowego magicznego słowa **!BDN** reprezentowanego przez bajty (0x21, 0x42, 0x44, 0x4E). Kolejna 2-bajtowa magiczna liczba, **SM** (0x53, 0x4D), znajduje się na przesunięciu 8 od początku pliku. Informacje o wersji (ANSI lub Unicode) są przesunięte o 10 od początku pliku. Wartość szesnastkowa (0x17) określa plik PST Unicode, podczas gdy 0x0E lub 0x0F reprezentuje format pliku ANSI.

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
|bidNextP (Unicode: 8 bajtów; ANSI: 4 bajty)|Następna strona BID. Strony posiadają specjalny licznik do przydzielania wartości bidIndex. Z tego licznika przydzielana jest wartość bidIndex dla BID-ów dla stron.
|bidNextB (tylko 4 bajty ANSI): |Następny BID. Ta wartość jest licznikiem monotonicznym, który wskazuje BID do przypisania dla następnego przydzielonego bloku. Wartości BID zwiększają się o 4. Więcej informacji znajduje się w sekcji 2.2.2.2.
|dwUnique (4 bajty)|Jest to monotonicznie rosnąca wartość, która jest modyfikowana za każdym razem, gdy modyfikowana jest struktura HEADER pliku PST. Funkcją tej wartości jest zapewnienie unikalnej wartości i zapewnienie, że CRC HEADER będą różne po każdej modyfikacji nagłówka.
|rgnid[] (128 bajtów)|Stała tablica 32 identyfikatorów NID, z których każdy odpowiada jednemu z 32 możliwych typów NID_TYPE (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_TYPE_ASSOC_MESSAGE)
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

### Ochrona danych ###

Ze względów bezpieczeństwa pliki PST mogą być również chronione hasłem, co wymaga, aby aplikacja ładująca zastosowała hasło, zanim będzie można je wyświetlić. Hasło zastosowane do pliku PST jest przechowywane w magazynie wiadomości. Nie zapewnia to jednak silnej ochrony danych, ponieważ hasło można usunąć za pomocą dostępnych narzędzi. Ponadto hasło określone przez użytkownika nie jest używane jako część klucza do kodowania i dekodowania algorytmów szyfrujących. W związku z tym nie ma korzyści z ochrony danych przed dostępem osób nieupoważnionych. Przechowywanie hasła w postaci skrótu CRC-32 oryginalnego ciągu również sprawia, że jest to słaba metoda zabezpieczenia danych przed podejściem brute-force.

## Bibliografia ##

* [Format pliku folderów osobistych programu Outlook (.pst)](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [Specyfikacje formatu plików folderów osobistych] (https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

