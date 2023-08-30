{
  "date" : "2020-11-11",
  "keywords" :["NDF", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku MDF i interfejsy API, które mogą tworzyć i otwierać pliki NDF.",
  "title" :"Format pliku NDF — główny plik bazy danych programu SQL Server",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Czym jest plik NDF?

Plik z rozszerzeniem .ndf to dodatkowy plik bazy danych używany przez [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) do przechowywania danych użytkownika. NDF jest plikiem pamięci dodatkowej, ponieważ serwer SQL przechowuje dane określone przez użytkownika w pliku pamięci podstawowej znanym jako [MDF](/pl/database/mdf/). Plik danych NDF jest opcjonalny i jest zdefiniowany przez użytkownika w celu zarządzania przechowywaniem danych w przypadku, gdy podstawowy plik MDF wykorzystuje całą przydzieloną przestrzeń. Zwykle jest przechowywany na oddzielnym dysku i może rozprzestrzeniać się na wiele urządzeń pamięci masowej. Obecność plików MDF jest niezbędna do otwarcia plików NDF.

## Format pliku NDF

Format pliku NDF nie różni się od formatu [MDF](/pl/database/mdf/) i wykorzystuje strony jako podstawową jednostkę przechowywania danych. każda strona zaczyna się od 96-bajtowego nagłówka, który zawiera:

* Identyfikator strony
* Typ konstrukcji
* Liczba rekordów na stronach
* Wskaźniki do poprzednich i następnych stron

### Struktura pliku NDF

Plik MDF ma następującą strukturę danych.

* Strona 0: Nagłówek
* Strona 1: Pierwszy PFS
* Strona 2: Pierwsza gra
* Strona 3: Pierwszy SGAM
* Strona 4: Nieużywane
* Strona 5: Nieużywane
* Strona 6: Pierwszy DCM
* Strona 7: Pierwszy BCM

#### Nagłówek pliku NDF

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

## Strona pliku danych

Strony w pliku danych programu SQL Server zaczynają się od zera (0) i zwiększają się sekwencyjnie. Każdy plik jest rozpoznawany po unikalnym numerze identyfikacyjnym pliku. Para identyfikator pliku i numer strony jednoznacznie identyfikuje stronę w bazie danych. Przykład pokazujący numery stron w bazie danych jest jak na poniższym obrazku.

{{< figure src="../ndf.png" alt="Format pliku bazy danych NDF" >}}

W tym przykładzie przedstawiono numery stron w bazie danych zawierającej podstawowy plik danych o wielkości 4 MB i plik danych pomocniczych o rozmiarze 1 MB.

## Bibliografia

* [Pliki bazy danych i grupy plików](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver16)
* [Odłączanie i dołączanie bazy danych — SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Analiza pliku danych programu SQL Server Anatomia](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

