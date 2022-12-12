{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - format pliku programu Microsoft OneNote",
  "description":"Poznaj format pliku ONETOC2 i interfejsy API, które mogą tworzyć i otwierać pliki ONETOC2.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest ONETOC2? ##

Osoby, które pracowały z aplikacją [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) mogły zauważyć obecność plików .onetoc2 w folderze notatnika. Microsoft OneNote tworzy binarny plik .onetoc2 jako spis treści do przechowywania indeksu dotyczącego kolejności różnych sekcji notatek w notatniku. Notatnik to zbiór plików sekcji, które są przechowywane w tym samym katalogu. Plik .onetoc2 wykorzystuje zbiór właściwości do określania ustawień, takich jak kolejność sekcji w notatniku i kolor notatnika.

Notes tworzony w programie OneNote 2016 jest automatycznie zapisywany w nowym formacie pliku 2010-2016. Ten format będzie potrzebny, jeśli chcesz, aby wszystkie funkcje programu OneNote 2016, takie jak równania matematyczne i połączone notatki, działały poprawnie.

## Format pliku ONETOC2 ##

Format pliku .onetoc2 jest reprezentowany jako OneNote Revision Store File Format i jest zbiorem struktur określających składnicę poprawek zorganizowaną w powiązane przestrzenie obiektów, zawierające obiekty z zestawami właściwości i zawierające dziennik transakcji w celu zapewnienia integralności plików w asynchronicznych pisze. Pełne specyfikacje formatu pliku .onetoc2 są dostępne [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) i można się do nich odnieść przy opracowywaniu aplikacji .

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
:


|Format pliku|Wartość
--- | --- |
|.jeden|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bajty):` Liczba całkowita bez znaku. MUSI być jedną z wartości w poniższej tabeli, w zależności od formatu tego pliku.


|Format pliku|Wartość
--- | --- |
|.jeden|0x0000002A
|.onetoc2|0x0000001B

## Bibliografia ##

* [[MS-ONESTORE] — format pliku programu OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote – Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

