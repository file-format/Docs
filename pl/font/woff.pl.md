{
  "date" : "2020-08-20",
  "keywords" :[ "plik woff", "format pliku woff", "co to jest plik woff", "plik", "przykład woff", "rozszerzenie pliku woff", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Web Open File Format",
  "description":"Plik WOFF to otwarty format czcionki utworzony w formacie Web Open Font Format.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## Czym jest plik WOFF?

Plik z rozszerzeniem .woff to plik czcionki internetowej oparty na formacie Web Open Font Format (WOFF). Ma specyficzny dla formatu skompresowany kontener oparty na typach czcionek TrueType (.TTF) lub OpenType (.OTT). WOFF został wprowadzony w celu odróżnienia czcionek internetowych od plików czcionek używanych w aplikacjach komputerowych. Ponadto format ma na celu zmniejszenie opóźnień w przesyłaniu czcionek z serwera do komputera klienta przez sieć. Dostępnych jest kilka narzędzi, które mogą konwertować pliki WOFF na TTF i inne formaty plików czcionek.

## **Format pliku WOFF**

Format czcionki WOFF kompresuje tabele danych czcionek struktur sfnt opartych na tabelach, używanych w różnych typach czcionek, takich jak TrueType, OpenType i Open Font Format. Jest jak kontener dla tych typów czcionek, a także ma miejsce na umieszczenie metadanych czcionki i danych do użytku prywatnego, które mają być zawarte w kontenerze. Konwertery używają plików sfnt do pliku w formacie WOFF, a programy klienckie przywracają zakodowany plik do użytku z dokumentem internetowym. Należy zauważyć, że przywrócone dane czcionki dokładnie odpowiadają wejściowemu formatowi czcionki pod każdym względem.

Narzędzia plików WOFF często zawierają dodatkowe funkcje, takie jak podzbiory glifów, sprawdzanie poprawności lub dodawanie funkcji czcionek, ale nie jest to konieczne. Zarówno twórca, jak i agenci użytkowania muszą zapewnić zachowanie ważności podstawowych danych czcionek.

### Struktura pliku WOFF

Struktura plików WOFF jest podobna do struktury czcionek sfnt. Opiera się na katalogu tabel, który zawiera długości i przesunięcia do każdej tabeli danych czcionek. Wszystkie tabele są przestrzegane po tej wstępnej informacji. Plik zawiera bazę czcionek, które są takie same jak w oryginalnych czcionkach. Kolejność tabel jest również taka sama, ale każda z nich może być skompresowana. Katalog tabeli WOFF zastępuje jednak oryginalny katalog tabeli.

Plik WOFF składa się z następujących elementów:

* WOFFHeader - Nagłówek pliku z podstawowym typem i wersją czcionki, wraz z przesunięciami do metadanych i prywatnych bloków danych.
* TableDirectory - Katalog tabel czcionek, wskazujący oryginalny rozmiar, skompresowany rozmiar i lokalizację każdej tabeli w pliku WOFF.
* FontTables - Tabele danych czcionek z wejściowej czcionki sfnt, skompresowane w celu zmniejszenia wymagań dotyczących przepustowości.
* ExtendedMetadata — opcjonalny blok rozszerzonych metadanych, reprezentowany w formacie XML i skompresowany do przechowywania w pliku WOFF.
* PrivateData — Opcjonalny blok prywatnych danych do wykorzystania przez projektanta czcionek, odlewnię lub dostawcę.

### Nagłówek WOFF
Nagłówek WOFF składa się z sygnatury identyfikującej, która wskazuje na rodzaj danych zawartych w pliku. Nagłówek WOFF wraz z jego polami wygląda następująco.

|Typ|Nazwa pola|Opis|
---|---|---|
|UInt32|podpis |0x774F4646 'wOFF' |
|UInt32| smak |"Wersja sfnt" czcionki wejściowej.|
|UInt32| długość |Całkowity rozmiar pliku WOFF.|
|UInt16| numTables |Liczba wpisów w katalogu tablic czcionek.|
|UInt16| zarezerwowane |Zarezerwowane; ustawione na zero.|
|UInt32| totalSfntSize |Całkowity rozmiar potrzebny dla nieskompresowanych danych czcionki, w tym nagłówka sfnt, katalogu i tabel czcionek (w tym dopełnienia).|
|UInt16| majorVersion |Główna wersja pliku WOFF.|
|UInt16| minorVersion |Mniejsza wersja pliku WOFF.|
|UInt32| metaOffset |Przesunięcie do bloku metadanych, od początku pliku WOFF.|
|UInt32| metaLength |Długość skompresowanego bloku metadanych.|
|UInt32| metaOrigLength |Nieskompresowany rozmiar bloku metadanych.|
|UInt32| privOffset |Przesunięcie do prywatnego bloku danych, od początku pliku WOFF.|
|UInt32| privLength |Długość prywatnego bloku danych.|


## **Bibliografia**
* [Format pliku w3 WOFF] (https://www.w3.org/TR/WOFF/)

