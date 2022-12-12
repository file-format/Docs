{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "plik sdf", "czym jest plik sdf", "jak otworzyć plik sdf", "rozszerzenie", "plik", "format pliku sdf", "Typ pliku bazy danych", "Format pliku bazy danych ", "Pliki bazy danych" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku SDF i interfejsy API, które mogą tworzyć i otwierać pliki SDF.",
  "title" :"SDF - Kompaktowy plik bazy danych programu SQL Server",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## Czym jest plik SDF?
Plik z rozszerzeniem .sdf zawiera bazę danych Microsoft SQL Server Compact (SQL CE), która jest również znana jako kompaktowa relacyjna baza danych; produkowane przez firmę Microsoft dla aplikacji tworzonych na urządzenia mobilne i komputery stacjonarne. Obsługuje zarówno 32-, jak i 64-bitowy system operacyjny, a cała zawartość bazy danych zawarta jest w jednym pliku SDF i może zajmować ponad 4 GB miejsca na dysku. Ze względów bezpieczeństwa plik .sdf można zaszyfrować przy użyciu szyfrowania 128-bitowego. Środowisko wykonawcze SQL CE ustala równoległy dostęp wielu użytkowników do pliku .sdf. Plik SDF można skopiować za pomocą **QuickOnce** lub po prostu skopiować do miejsca docelowego w celu wdrożenia systemu.

## Format pliku SDF
Plik SDF zawiera bazę danych, która jest zwykle nazywana kompaktową relacyjną bazą danych. Plik SDF zawiera wszystkie informacje związane z bazą danych, a SQL Server Compact to lekki i darmowy silnik bazy danych, który służy do zarządzania plikami .sdf. Rozmiar pliku .sdf nie powinien przekraczać limitu 4 GB. Pliki SDF nie przechowują informacji o procedurach przechowywanych, wyzwalaczach ani widokach. Aplikacje korzystające z bazy danych SQL CE nie muszą określać ścieżki do pliku SDF w ciągu połączenia ADO.NET, zamiast tego można ją wymienić jako |DataDirectory|\database_name.sdf, definiując katalog danych zdefiniowany w manifeście asemblera dla aplikacji
Konwencja nazewnictwa .sdf jest opcjonalna, a do zapisania pliku można użyć dowolnego rozszerzenia. Ustawienie hasła do pliku bazy danych jest krokiem opcjonalnym. Aby skompresować lub naprawić bazę danych należy zapisać plik z opcją **kompaktowana/naprawiona baza danych**.

## Bibliografia

* [SQL Server Compact – Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [Korzystanie z SQL Server Compact dla aplikacji internetowych ASP.NET](https://docs.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


