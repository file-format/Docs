{
  "date" : "2020-11-11",
  "keywords" :["LDF", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku LDF i interfejsy API, które mogą tworzyć i otwierać pliki LDF.",
  "title" :"LDF — format pliku głównej bazy danych programu SQL Server",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Czym jest plik LDF?

Plik z rozszerzeniem .ldf to plik dziennika obsługiwany przez Microsoft SQL Server, który jest systemem zarządzania relacyjnymi bazami danych (RDBMS). Wszystkie transakcje wykonywane na plikach podstawowej bazy danych ([MDF](/pl/database/mdf/))(takie jak wstawianie, aktualizacja, usuwanie) są rejestrowane w pliku LDF. Pliki LDF są krytycznymi składnikami każdej bazy danych. W przypadku awarii systemu plik dziennika służy do przywrócenia bazy danych do stanu spójnego. Plik dziennika transakcji może się zwiększyć, jeśli transakcje nie są w pełni zatwierdzone. Pliki LDF można otwierać za pomocą aplikacji oprogramowania Microsoft SQL Server.

## Operacje zapisane w pliku LDF

Plik dziennika SQL rejestruje następujące operacje:

* Początek i koniec każdej transakcji.

* Każda modyfikacja danych danych (wstawianie, aktualizacja lub usuwanie). Obejmuje to również zmiany dokonywane przez systemowe procedury składowane lub instrukcje języka definicji danych (DDL) w dowolnej tabeli, w tym w tabelach systemowych.

* Każdy zakres i alokacja strony lub cofnięcie alokacji.

* Tworzenie lub usuwanie tabeli lub indeksu.

## Format pliku LDF

Plik LDF składa się z rekordów transakcji SQL Server, które są ułożone jako ciąg rekordów dziennika. Każdy rekord dziennika ma numer kolejny dziennika (LSN), który jest wyższy niż numer LSN poprzedniego rekordu. Ciągi są łączone jeden po drugim w pliku. Dzięki nowoczesnym, szybkim komputerom rekordy można wstawiać tam, gdzie w pliku dziennika znajduje się LSN2 przed LSN1. Ponieważ operacje są rejestrowane szeregowo, zmiana opisana przez LSN2 została wykonana po zapisie dziennika LSN1. Rekordy dla określonej transakcji są łączone wstecz za pomocą wskaźników, które są używane i przyspieszają wycofywanie transakcji.
 

## Bibliografia

* [Pliki bazy danych i grupy plików](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Przewodnik po architekturze i zarządzaniu dziennikami transakcji](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql- serwer-ver15)

