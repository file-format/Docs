{
  "date" : "2020-11-11",
  "keywords" :["MDB", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku MDB i interfejsy API, które mogą tworzyć i otwierać pliki MDB.",
  "title" :"Format pliku MDB — plik bazy danych programu Microsoft Access",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Czym jest plik MDB?

Plik z rozszerzeniem .mdb to plik bazy danych Microsoft Access, który jest systemem zarządzania relacyjną bazą danych (RDBMS). Przechowuje dane w tabelach bazy danych, które są ze sobą połączone za pomocą kluczy podstawowych i obcych. Plik MDB zawiera pełną strukturę tabel bazy danych, zapytań, procedur składowanych. MDB jest domyślnym formatem plików programu Microsoft Access 2003. Późniejsze wersje programu Microsoft Access używają formatu plików [ACCDB](/pl/database/accdb/), który jest jak dotąd najnowszym formatem plików. Pliki MDB można otwierać za pomocą aplikacji takich jak Microsoft Access, MDB Viewer, MDBOpener i można je konwertować do formatów ACCDB, [CSV] (/pl/spreadsheet/csv/), Excel itp.

## Format pliku MDB

Istnieją publiczne specyfikacje dostępne dla formatu MDB i pozostaje on zastrzeżonym formatem plików firmy Microsoft. Firma Microsoft zapewnia jednak dostęp do połączenia z plikiem MDB przy użyciu standardu Open Database Connectivity (ODBC) i języka Visual Basic for Applications (VBA). Nieoficjalny przewodnik MDB zawiera krótki, nieformalny opis formatu MDB oparty na inżynierii wstecznej i można się z nim zapoznać, aby poznać specyfikacje.

### Strony

Zgodnie z nieoficjalnym przewodnikiem MDB, plik MDB składa się ze stron o stałym rozmiarze (2048 bajtów dla Jeb DB3 i 4096 bajtów dla Jet DB 4). Pierwszy bajt wskazuje typ strony. Oto kluczowe typy stron:

`Pierwsza strona:` Zawiera informacje nagłówka bazy danych, które obejmują również identyfikację wersji Jet DB, z którą plik jest zgodny. Ponadto zawiera również informacje o bezpieczeństwie plików i mapę użytkowania strony.

`Strona definicji tabeli:` Strona definicji tabeli określa kolumny, typy danych, indeks i inne informacje. W razie potrzeby korzysta z dodatkowych stron i zawiera mapę stron zawierającą dane wierszy dla tej tabeli.

`Strony danych:` Strony danych to rzeczywiste kontenery danych, w których dane są przechowywane w wierszach. Używa stron pomocniczych do przechowywania długich wartości danych.

Pojedyncza baza danych Microsoft Access może składać się z wielu plików, co pozwala na przekroczenie ograniczeń wielkości plików i tabel. Ułatwia to umieszczanie formularzy i kodu w pliku front-end MDB na pulpicie użytkownika oraz danych w innych plikach MDB back-end na serwerach podłączonych do sieci.

## Bibliografia ##

* [Specyfikacje dostępu](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Nieoficjalny przewodnik MDB] (http://jabakobob.net/mdb/)

