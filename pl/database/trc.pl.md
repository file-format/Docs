{
  "date" : "2021-08-24",
  "keywords" :["plik trc", "format pliku trc", "co to jest plik trc", "plik", "przykład trc", "rozszerzenie pliku trc", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format plików TRC i interfejsy API, które mogą tworzyć i otwierać pliki TRC.",
  "title" :"TRC - plik śledzenia serwera SQL",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Czym jest plik TRC?
Plik z rozszerzeniem .trc zawiera wyniki śledzenia aktywności bazy danych serwera Miscrosoft SQL. Pliki te są tworzone przez oprogramowanie SQL Server Profiler; zwykle w pakiecie z oprogramowaniem Microsoft SQL Server. Administratorzy bazy danych mogą analizować sekwencję instrukcji bazy danych i przeglądać dziennik śledzenia, jeśli podejrzewane są jakieś błędy lub ostrzeżenia. Pliki te zwykle znajdują się w typowym folderze LOG MSSQL w katalogu Program Files w systemie operacyjnym Windows.

## Format pliku TRC
Format pliku TRC jest używany przez SQL Server Profiler do automatycznego generowania nowego śladu ostatnio wykonanych instrukcji przez serwer MS SQL. SQL Server Profiler używa szablonu domyślnego dla każdego nowego śledzenia. Oprogramowanie zawiera jednak kilka predefiniowanych szablonów do monitorowania określonych typów zdarzeń. Programu SQL Server Profiler można również używać do tworzenia szablonów definiujących klasy zdarzeń i kolumny danych, które mają być uwzględniane w śledzeniu.

### Wstępnie zdefiniowane szablony
Oto lista niektórych predefiniowanych szablonów zawartych w programie SQL Server Profiler:
- **SP_Counts**: Przechwytuje zachowanie wykonywania procedury składowanej w czasie.
- **Standard**: Ogólny punkt wyjścia do tworzenia śladu.
- **TSQL**: Przechwytuje wszystkie instrukcje języka Transact-SQL, które są przesyłane do programu SQL Server przez klientów, oraz czas ich wystawienia.
- **TSQL_Duration**: Przechwytuje wszystkie instrukcje Transact-SQL przesłane do SQL Server przez klientów, czas ich wykonania i grupuje je według czasu trwania.
- **TSQL_Grouped**: Służy do badania zapytań od określonego klienta lub użytkownika.
- **TSQL_Locks**: Służy do rozwiązywania problemów z zakleszczeniami, limitu czasu blokady i zdarzeń eskalacji blokady.
- **TSQL_Replay**: Służy do przeprowadzania dostrajania iteracyjnego, takiego jak testy porównawcze.
- **TSQL_SPs**: Służy do analizowania kroków składowych procedur składowanych.
- **Dostrajanie**: Służy do generowania danych wyjściowych śledzenia, których Doradca dostrajania aparatu bazy danych może używać jako obciążenia do dostrajania baz danych.
### Skoreluj śledzenie z danymi dziennika wydajności systemu Windows
SQL Server Profiler może być używany do otwierania dziennika wydajności Microsoft Windows, wybierania liczników do skorelowania ze śladem i wyświetlania wybranych liczników wydajności obok śladu w GUI MS SQL Server Profiler. Aby wskazać dane dziennika wydajności, które są skorelowane z wybranym zdarzeniem śledzenia, pionowy czerwony pasek w okienku danych Monitora systemu programu SQL Server Profiler.


## Bibliografia ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

