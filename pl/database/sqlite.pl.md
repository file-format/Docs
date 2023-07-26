{
  "date" : "2019-12-12",
  "keywords" :["SQLite", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku SQLITE i interfejsy API, które mogą tworzyć i otwierać pliki SQLITE.",
  "title" :"Format pliku SQLite",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Co to jest plik SQLite?

Plik z rozszerzeniem .sqlite to lekki plik bazy danych SQL utworzony za pomocą oprogramowania [SQLite](https://www.sqlite.org/index.html). Jest to baza danych w samym pliku i implementuje samodzielny, w pełni funkcjonalny, wysoce niezawodny silnik bazy danych [SQL](/pl/database/sql/). Pliki bazy danych SQLite mogą być używane do udostępniania bogatej zawartości między systemami poprzez prostą wymianę tych plików w sieci. Prawie wszystkie telefony komórkowe i komputery używają SQLite do przechowywania i udostępniania danych, a także jest to wybór formatu plików dla aplikacji wieloplatformowych. Ze względu na kompaktowe zastosowanie i łatwą obsługę jest dostarczany w pakiecie z innymi aplikacjami. Istnieją powiązania SQLite dla języków programowania, takich jak C, [C#](/pl/programming/cs/), [C++](/pl/programming/cpp), [Java](/pl/programming/java/), [PHP](/pl/programming/php/ ), i wiele innych.

## Format pliku SQLite

SQLite w rzeczywistości jest biblioteką C-Language, która implementuje SQLite RDBMS przy użyciu formatu pliku SQLite. Wraz z ewolucją nowych urządzeń każdego dnia, jego format plików został zachowany we wstecznej kompatybilności, aby pomieścić starsze urządzenia. Format pliku SQLite jest postrzegany jako długoterminowy format archiwizacji danych.

### Plik bazy danych

Baza danych SQLite jest w pełni obsługiwana za pomocą dwóch plików.
* Główny plik bazy danych - Zawiera pełny stan bazy danych SQLite
* Rollback Journal - Przechowuje dodatkowe informacje w drugim pliku i jest używany podczas wykonywania transakcji. W przypadku, gdy SQLite jest w trybie WAL, utrzymywany jest plik dziennika głowicy zapisu.

#### Plik dziennika

Ten plik ma na celu przechowywanie wszystkich informacji przechowywanych na wypadek, gdyby ostatnia transakcja nie mogła zostać zakończona w przypadkach takich jak awaria komputera. Ten plik służy do przywracania pliku bazy danych do spójnego stanu.

#### Strony

Główny plik bazy danych SQLite składa się z jednej lub więcej stron. W dowolnym momencie każda strona w głównej bazie danych ma jedno zastosowanie, które jest jednym z następujących:

* Strona z bajtem blokującym
* Wolna strona
* Wolna strona bagażnika
* Wolna strona liścia
* Strona b-drzewa
* Strona wewnętrzna b-drzewa tabeli
* Strona liścia tabeli b-drzewo
* Strona wewnętrzna indeksu b-drzewa
* Strona liści indeksu b-drzewa
* Strona przepełnienia ładunku
* Strona mapy wskaźników

Rozmiar plików bazy danych SQLite może wahać się od kilku kilobajtów do kilku gigabajtów.

### Nagłówek SQLite

Nagłówek bazy danych SQLite znajduje się w pierwszych 100 bajtach pliku bazy danych. Każdy prawidłowy plik bazy danych SQLite zaczyna się od 16 bajtów (heksadecymalnie): 53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Szczegóły dotyczące pól nagłówka przedstawiono w poniższej tabeli.

|Przesunięcie|Rozmiar|Opis|
---|---|---|
|0|16|Ciąg nagłówka: "SQLite format 3\000"|
|16|2|Rozmiar strony bazy danych w bajtach. Musi być potęgą dwójki z zakresu od 512 do 32768 włącznie lub wartość 1 reprezentująca rozmiar strony 65536.|
|18|1|Wersja zapisu formatu pliku. 1 dla dziedzictwa; 2 dla WAL.|
|19|1|Format pliku wersja do odczytu. 1 dla dziedzictwa; 2 dla WAL.|
|20|1|Bajty niewykorzystanego „zarezerwowanego” miejsca na końcu każdej strony. Zwykle 0.|
|21|1|Maksymalna część wbudowanego ładunku. Musi być 64.|
|22|1|Minimalna część wbudowanego ładunku. Musi być 32.|
|23|1|Ułamek ładunku liści. Musi być 32.|
|24|4|Licznik zmian plików.|
|28|4|Rozmiar pliku bazy danych w stronach. "Rozmiar bazy danych w nagłówku".|
|32|4|Numer strony pierwszej strony głównej wolnej listy.|
|36|4|Całkowita liczba stron z wolnymi listami.|
|40|4|Plik cookie schematu.|
|44|4|Numer formatu schematu. Obsługiwane formaty schematów to 1, 2, 3 i 4.|
|48|4|Domyślny rozmiar pamięci podręcznej strony.|
|52|4|Numer strony największego korzenia b-drzewa w trybie automatycznego odkurzania lub przyrostowego odkurzania lub zero w przeciwnym przypadku.|
|56|4|Kodowanie tekstu bazy danych. Wartość 1 oznacza UTF-8. Wartość 2 oznacza UTF-16le. Wartość 3 oznacza UTF-16be.|
|60|4|"Wersja użytkownika" odczytana i ustawiona przez pragma user_version.|
|64|4|Prawda (niezerowa) dla trybu próżni przyrostowej. Fałsz (zero) w przeciwnym razie.|
|68|4|"Identyfikator aplikacji" ustawiony przez PRAGMA application_id.|
|72|20|Zarezerwowane do rozbudowy. Musi być zero.|
|92|4|Numer ważnej wersji.|
|96|4|SQLITE_VERSION_NUMBER|

## Bibliografia ##

* [Format pliku SQLite — SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite — specyfikacja języka C](https://www.sqlite.org/c3ref/intro.html)

