{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JEDEN — format pliku programu Microsoft OneNote",
  "description":"Dowiedz się o JEDNYM formacie pliku i interfejsach API, które mogą tworzyć i otwierać JEDEN plik.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest plik .ONE? ##

Pliki reprezentowane przez rozszerzenie .ONE są tworzone przez aplikację Microsoft OneNote. Program OneNote umożliwia zbieranie informacji za pomocą aplikacji tak, jakbyś używał notatnika roboczego do robienia notatek. Pliki programu OneNote mogą zawierać różne elementy, które można umieszczać w nieustalonych lokalizacjach na stronach dokumentów. Elementy te mogą zawierać tekst, cyfrowe pismo odręczne i obiekty skopiowane z innych aplikacji, w tym obrazy, rysunki i klipy multimedialne (audio/wideo). Firma Microsoft oferuje teraz wersję online programu OneNote w ramach usługi Office365, w której notatki można udostępniać innym użytkownikom programu OneNote przez Internet.

## Specyfikacje formatu plików .ONE ##

Format pliku programu OneNote zapewnia skuteczny sposób przedstawiania notatek cyfrowych jako hierarchicznych zestawów sekcji i stron. Każda strona zawiera treść zdefiniowaną przez użytkownika w określonej strukturze do reprezentacji w formacie pliku Document Object Model (DOM). Model danych dla tego formatu jest przedstawiony poniżej.

### Przegląd struktury ###

Jak pokazano w modelu danych dla formatu pliku programu OneNote, dokument programu OneNote składa się z różnych elementów.

#### Sekcja ####

Sekcja to najwyższy kontener w pliku programu OneNote, który dodatkowo zawiera różne elementy, takie jak:

* Strony
* Metadane
* Nieruchomości

Metadane i właściwości obejmują nazwę sekcji, identyfikację stron zawartych w sekcji oraz kolejność, w jakiej pojawiają się te strony. Termin „sekcja” odnosi się do wszystkich stron znajdujących się w sekcji oraz reprezentacji tych danych w pliku magazynu wersji programu OneNote®, który ma rozszerzenie nazwy pliku .one.

#### Strona ####

Zawartość zdefiniowana przez użytkownika w dokumencie programu OneNote jest zawarta na stronie. Informacje o stronie obejmują tekst, listy, tabele, tytuły stron, obrazy i znaczniki notatek. Strona składa się z obiektów konspektu, do których dodawana jest większość znajdujących się w nich obiektów. Każdej stronie można przypisać nazwę w celu reprezentacji, a obiekty można dodawać bezpośrednio do stron. Strona może ponadto zawierać podstrony w systemie hierarchicznym.

#### Właściwości i zestawy właściwości ####

Zawartość programu OneNote składa się z właściwości, zestawów właściwości i obiektów danych pliku. Zestaw właściwości to zbiór właściwości, który reprezentuje pewien typ zawartości. Obiekt danych pliku to blok danych binarnych, który zawiera obrazy, osadzone pliki lub treści audio/wideo.

#### Notatnik programu OneNote ####

Notatnik to zbiór plików sekcji, które są przechowywane w tym samym katalogu. Zbiór właściwości służy do określania ustawień, takich jak kolejność sekcji w notatniku i kolor notatnika.

### Struktura plików ###

Plik magazynu wersji MUSI zaczynać się od struktury **Nagłówek**. Pozostała część pliku jest podzielona na bloki bajtów, gdzie rozmiar i struktura każdego bloku jest określona przez pole, które się do niego odwołuje. Blok jest osiągalny, jeśli odwołuje się do niego struktura **Nagłówek** lub jeśli odwołuje się do niego pole w innym osiągalnym bloku. Dane poza strukturą **Header** i wszelkie osiągalne bloki MUSZĄ być ignorowane.

Wszystkie struktury są wyrównane na granicach 1-bajtowych. Wszystkie liczby całkowite są podpisane, chyba że określono inaczej. Wszystkie pola to [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), chyba że określono inaczej.

#### Nagłówek ####

Nagłówek pliku .ONE składa się z fragmentów, które zawierają różne unikalne identyfikatory i pola do reprezentacji informacji o pliku w następujący sposób:

`guidFileType (16 bajtów):` Identyfikator GUID określający typ pliku magazynu wersji. MUSI być jedną z wartości z poniższej tabeli.


|Format pliku|Wartość
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bajtów):` Identyfikator GUID określający tożsamość tego pliku magazynu wersji. POWINIEN być unikatowy na skalę światową.

`guidLegacyFileVersion (16 bajtów):` MUSI być "{00000000-0000-0000-0000-000000000000}" i MUSI być ignorowane.

`guidFileFormat (16 bajtów):` Identyfikator GUID określający, że plik jest plikiem magazynu wersji. MUSI być „{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}”.

`ffvLastCodeThatWroteToThisFile (4 bajty):` Liczba całkowita bez znaku. MUSI być jedną z wartości w poniższej tabeli, w zależności od typu pliku.

|Format pliku|Wartość
--- | --- |
|.jeden|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 bajty):` Liczba całkowita bez znaku. MUSI być jedną z wartości w poniższej tabeli, w zależności od formatu tego pliku.


|Format pliku|Wartość
--- | --- |
|.jeden|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bajty):` Liczba całkowita bez znaku. MUSI być jedną z wartości w poniższej tabeli, w zależności od formatu tego pliku.

|Format pliku|Wartość
--- | --- |
|.jeden|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bajty):` Liczba całkowita bez znaku. MUSI być jedną z wartości w poniższej tabeli, w zależności od formatu tego pliku.

|Format pliku|Wartość
--- | --- |
|.jeden|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 bajtów):` Struktura **FileChunkReference32** MUSI mieć wartość „fcrZero”.

`fcrLegacyTransactionLog (8 bajtów):` Struktura **FileChunkReference32** MUSI mieć wartość „fcrNil”.

`cTransactionsInLog (4 bajty):` Liczba całkowita bez znaku określająca liczbę transakcji w dzienniku transakcji. NIE MOŻE być zerem.

`cbLegacyExpectedFileLength (4 bajty):` Liczba całkowita bez znaku, która MUSI być równa zero i MUSI być ignorowana.

`rgbPlaceholder (8 bajtów):` Liczba całkowita bez znaku, która MUSI być równa zero i MUSI być ignorowana.

`fcrLegacyFileNodeListRoot (8 bajtów):` Struktura **FileChunkReference32**, która MUSI mieć wartość „fcrNil”.

`cbLegacyFreeSpaceInFreeChunkList (4 bajty):` Liczba całkowita bez znaku, która MUSI być równa zero i MUSI być ignorowana.

`fNeedsDefrag (1 bajt):` MUSI być ignorowane.

`fRepairedFile (1 bajt):` MUSI być ignorowane.

`fNeedsGarbageCollect (1 bajt):` MUSI być ignorowane.

`fHasNoEmbeddedFileObjects (1 bajt):` Liczba całkowita bez znaku, która MUSI być równa zero i MUSI być ignorowana.

`guidAncestor (16 bajtów):` Identyfikator GUID określający pole **Header.guidFile** pliku spisu treści podanego w poniższej tabeli:


|Format pliku spisu treści|Lokalizacja pliku spisu treści
--- | --- |
|Plik sekcji — .Jeden|Plik spisu treści znajduje się w tym samym katalogu co ten plik.
|Plik spisu treści — .onetoc2|Plik spisu treści znajduje się w katalogu nadrzędnym tego pliku.

Jeśli identyfikator GUID to {00000000-0000-0000-0000-000000000000}, to pole nie odwołuje się do pliku spisu treści.

`crcName (4 bajty):` Liczba całkowita bez znaku, która określa wartość CRC nazwy tego pliku magazynu wersji. Nazwa jest reprezentacją Unicode nazwy pliku z rozszerzeniem i dodatkowym znakiem null na końcu. To CRC jest zawsze obliczane przy użyciu algorytmu CRC dla pliku .one, niezależnie od tego formatu pliku magazynu wersji.

`fcrHashedChunkList (12 bajtów):` Struktura **FileChunkReference64x32**, która określa odwołanie do pierwszego **FileNodeListFragment** na zaszyfrowanej liście fragmentów. Jeśli wartość struktury **FileChunkReference64x32** to „fcrZero” lub „fcrNil”, zaszyfrowana lista fragmentów nie istnieje.

`fcrTransactionLog (12 bajtów):` Struktura **FileChunkReference64x32** określająca odniesienie do pierwszej struktury **TransactionLogFragment** w dzienniku transakcji. Wartość pola **fcrTransactionLog** NIE MOŻE być „fcrZero” i NIE MOŻE być „fcrNil”.

`fcrFileNodeListRoot (12 bajtów):` Struktura **FileChunkReference64x32** określająca odwołanie do listy węzłów pliku głównego. Wartość pola **fcrFileNodeListRoot** NIE MOŻE być „fcrZero” i NIE MOŻE być „fcrNil”.

`fcrFreeChunkList (12 bajtów):` Struktura **FileChunkReference64x32** określająca odwołanie do pierwszej struktury **FreeChunkListFragment**. Jeśli wartością struktury **FileChunkReference64x32** jest „fcrZero” lub „fcrNil”, to lista wolnych porcji nie istnieje.

`cbExpectedFileLength (8 bajtów):` Liczba całkowita bez znaku określająca rozmiar w bajtach tego pliku składnicy poprawek.

`cbFreeSpaceInFreeChunkList (8 bajtów):` Liczba całkowita bez znaku, która POWINNA określać w bajtach rozmiar wolnego miejsca określonego przez listę wolnych porcji.

`guidFileVersion (16 bajtów):` Identyfikator GUID. Gdy wartość pola **cTransactionsInLog** lub **guidDenyReadFileVersion** jest zmieniana, **guidFileVersion** MUSI zostać zmieniony na nowy identyfikator GUID.

`nFileVersionGeneration (8 bajtów):` Liczba całkowita bez znaku określająca, ile razy plik został zmieniony. MUSI być zwiększana, gdy zmienia się pole **guidFileVersion**.

`guidDenyReadFileVersion (16 bajtów):` Identyfikator GUID. Gdy zmieniana jest istniejąca zawartość pliku, z wyłączeniem struktury **Nagłówka** pliku i nieużywanych bloków pamięci, **guidDenyReadFileVersion** MUSI zostać zmieniony na nowy identyfikator GUID.

`grfDebugLogFlags (4 bajty):` MUSI mieć wartość zero. MUSI być ignorowane.

`fcrDebugLog (12 bajtów):` Struktura **FileChunkReference64x32**, która MUSI mieć wartość „fcrZero”. MUSI być ignorowane.

`fcrAllocVerificationFreeChunkList (12 bajtów):` Struktura **FileChunkReference64x32** MUSI mieć wartość „fcrZero”. MUSI być ignorowane.

`bnCreated (4 bajty):` Liczba całkowita bez znaku, która określa numer kompilacji aplikacji, która utworzyła ten plik magazynu wersji. POWINNO być ignorowane.

`bnLastWroteToThisFile (4 bajty):` Liczba całkowita bez znaku, która określa numer kompilacji aplikacji, która ostatnio zapisała w tym pliku składnicy poprawek. POWINNO być ignorowane.

`bnOldestWritten (4 bajty):` Liczba całkowita bez znaku, która określa numer kompilacji najstarszej aplikacji, która zapisała w tym pliku składnicy poprawek. POWINNO być ignorowane.

`bnNewestWritten (4 bajty):` Liczba całkowita bez znaku, która określa numer kompilacji najnowszej aplikacji, która zapisała w tym pliku składnicy poprawek. POWINNO być ignorowane.

`rgbReserved (728 bajtów):` MUSI mieć wartość zero. MUSI być ignorowane.

## Bibliografia ##

* [[MS-ONESTORE] — format pliku programu OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote – Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

