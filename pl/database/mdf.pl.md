{
  "date" : "2020-11-11",
  "keywords" :["MDF", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku MDF i interfejsy API, które mogą tworzyć i otwierać pliki MDF.",
  "title" :"Format pliku MDF — główny plik bazy danych programu SQL Server",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Czym jest plik MDF?

Plik z rozszerzeniem .mdf jest głównym plikiem bazy danych używanym przez [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) do przechowywania danych użytkownika. Ma to pierwszorzędne znaczenie, ponieważ wszystkie dane są przechowywane w tym pliku. Plik MDF przechowuje dane użytkowników w relacyjnych bazach danych w postaci kolumn, wierszy, pól, indeksów, widoków i tabel. SQL Server pozwala ustawić ustawienia automatycznego powiększania i automatycznego zmniejszania, aby mieć pozytywny wpływ na wydajność bazy danych. Pliki MDF można ładować i dołączać do bazy danych za pomocą Microsoft SQL Server. Pliki MDF mają typ mime Application/octet-stream.

## Format pliku MDF

Podstawową jednostką przechowywania danych w SQL Server jest strona. Strona pamięci przypisanej do bazy danych jest podzielona na strony logiczne o numerach od 0 do n. Pojedyncza strona zaczyna się od 96-bajtowego nagłówka, który zawiera identyfikator strony, typ struktury, do której należy strona, liczbę rekordów na stronie oraz wskaźniki do poprzedniej i następnej strony.

### Struktura plików

Plik MDF ma następującą strukturę danych.

* Strona 0: Nagłówek
* Strona 1: Pierwszy PFS
* Strona 2: Pierwsza gra
* Strona 3: Pierwszy SGAM
* Strona 4: Nieużywane
* Strona 5: Nieużywane
* Strona 6: Pierwszy DCM
* Strona 7: Pierwszy BCM

#### Nagłówek pliku

Strona numer 0 wszystkich plików zawiera nagłówek, w którym przechowywane są metadane dotyczące pliku.

#### Wolne miejsce na stronie (PFS)
PFS identyfikuje stan alokacji i określa ilość wolnego miejsca.

* Bit 1: Wskazuje, czy strona jest przydzielona, czy nie.
* Bit 2: Wskazuje, czy strona pochodzi z mieszanego zasięgu.
* Bit 3: wskazuje, że ta strona jest stroną IAM.
* Bit 4: Wskazuje, że ta strona zawiera rekordy duchów
* Bity od 5 do 7: połączona wartość trzybitowa, która wskazuje zapełnienie strony w następujący sposób:
* 0: Strona jest pusta
* 1: Strona jest zapełniona w 1–50%.
* 2: Strona jest zapełniona w 51–80%.
* 3: Strona jest zapełniona w 81–95%.
* 4: Strona jest zapełniona w 96–100%.

## Bibliografia

* [Pliki bazy danych i grupy plików](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Odłączanie i dołączanie bazy danych — SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [Analiza pliku danych programu SQL Server Anatomia](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

