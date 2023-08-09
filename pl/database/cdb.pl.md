{
  "date" : "2021-06-16",
  "keywords" :["CDB", "rozszerzenie", "plik cdb", "format pliku cdb", "Typ pliku bazy danych", "Format pliku bazy danych", "co to jest plik cdb" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku CDB i interfejsy API, które mogą tworzyć i otwierać pliki CDB.",
  "title" :"CDB - Stały Plik Bazy Danych",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## Czym jest plik CDB?
Pliki CDB są używane w aplikacjach o znaczeniu krytycznym, takich jak poczta e-mail. CDB oznacza „constant database”, szybki, niezawodny i prosty pakiet do tworzenia lub odczytywania stałych baz danych. Wymiana bazy danych jest bezpieczna przed awariami systemu. Użytkownicy nie muszą przerywać pracy podczas przepisywania. CDB działa jako tablica asocjacyjna (na dysku), odwzorowując klucze na wartości i umożliwia przechowywanie wielu wartości w jednym kluczu.

## Format pliku CDB
Format pliku CDB przechowuje liczby, przesunięcia, długości i wartości skrótu w formacie little endian jako 32-bitowe liczby całkowite bez znaku. Uważa się, że klucze i dane to nieprzezroczyste ciągi bajtów bez specjalnego traktowania. Na początku bazy danych nagłówek o stałym rozmiarze reprezentuje 256 tablic skrótów, wymieniając ich pozycję w pliku i ich długość w szczelinach. Zwykle dane są przechowywane jako sekwencja rekordów, każdy rekord przechowuje długość klucza, długość danych, klucz i dane. Nie ma reguł sortowania ani wyrównywania. Po rekordach następuje zestaw 256 tablic mieszających o różnej długości. Ponieważ zero jest poprawną długością, w bazie danych może być fizycznie przechowywanych mniej niż 256 tabel skrótów, ale nic nie jest uważane za 256 tabel. Tabele skrótów składają się z szeregu gniazd, z których każdy zawiera wartość skrótu i przesunięcie rekordu. „Puste gniazda” mają przesunięcie równe zero.

### Struktura
Baza danych CDB składa się z całego zestawu danych w jednym pliku komputerowym. Zawiera trzy części:
- Nagłówek o stałym rozmiarze
- Dane
- Zestaw tablic mieszających.

Wyszukiwania są dostępne tylko dla kluczy dokładnych. Wyszukiwania działają przy użyciu następującego algorytmu:

- Zaszyfruj klucz.
- Określ, w której tablicy skrótów i gnieździe powinien znajdować się ten rekord.
- Przetestuj wskazane miejsce w tabeli skrótów.

W przypadku wyszukiwania kluczy z więcej niż jedną wartością dodatkowe wartości można znaleźć po prostu wznawiając wyszukiwanie w następnym gnieździe.

#### Cechy

Struktura bazy danych CDB zapewnia kilka funkcji:

##### Szybkie wyszukiwanie
Udane wyszukiwanie w ogromnej bazie danych zwykle wymaga tylko dwóch dostępów do dysku, a nieudane wyszukiwanie wymaga tylko jednego.
##### Niskie koszty ogólne
Baza danych wykorzystuje 2048 bajtów, 24 bajty na rekord oraz miejsce na klucze i dane.
##### Brak losowych limitów
CDB może zarządzać dowolną bazą danych do 4 gigabajtów. Ponieważ nie ma innych ograniczeń, rekordy nie muszą nawet mieścić się w pamięci. Bazy danych są przechowywane w formacie niezależnym od komputera.
##### Szybka wymiana atomowej bazy danych
Polecenie **cdbmake** może przepisać całą bazę danych do dwóch rzędów wielkości, szybciej niż inne pakiety haszujące.
##### Szybkie zrzuty bazy danych
**cdbdump** może drukować zawartość bazy danych w formacie zgodnym z cdbmake.


## Bibliografia ##

* [cdb (oprogramowanie) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(software))
* [Specyfikacja CDB](http://cr.yp.to/cdb.html)

