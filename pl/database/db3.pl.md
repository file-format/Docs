{
  "date" : "2019-12-12",
  "keywords" :["DB3", "Format pliku DB3", "Plik DB3", "SQLite", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych" ] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się więcej o formacie plików DB3 i interfejsach API, które mogą tworzyć i otwierać pliki DB3.",
  "title" :"Format pliku DB3",
  "linktitle" : "DB3",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Czym jest plik DB3?
Plik DB3 to plik bazy danych utworzony przez oprogramowanie SQLite, które jest lekkim, samodzielnym programem bazodanowym, który tworzy bazy danych przy użyciu zwykłych plików; zawiera anatomię bazy danych oraz rekordy danych; powszechnie używany do pobierania lub przechowywania danych strukturalnych przy użyciu języka SQL. Pliki te mogą być używane w inteligentnych urządzeniach lub tam, gdzie wymagane jest prowadzenie dokumentacji lub inne zarządzanie danymi, ale w środowisku o małej przestrzeni.


## Format pliku DB3
Format pliku DB3 jest powiązany z RDBMS (Relational Database Management System) SQLite, popularnym wyborem dla wbudowanej bazy danych. W specyfikacji SQLite_3 nie ma określonego rozszerzenia pliku, może on używać rozszerzeń, w tym [.dbf](/pl/database/dbf/) i [.sqlite](/pl/database/sqlite/).

### Zabezpieczenie bazy danych
Zwykle format pliku db związany z SQLite, wersja 3, może być uważany za format pliku DB3 używany jako publicznie udokumentowany natywny format silnika bazy danych SQLite od czerwca 2004 r. Format pliku DB3 jest wieloplatformowy, można go przenosić między big-endian i little-endian lub systemy 32-bitowe i 64-bitowe. Te cechy sprawiają, że DB3 jest popularnym formatem plików aplikacji. Główny plik bazy danych SQLite_3 (DB3) składa się z co najmniej jednej strony. Wszystkie rozmiary wszystkich stron są równe w tej samej bazie danych. Rozmiar strony w bajtach to potęga dwójki z przedziału od 512 do 65536 włącznie.



## Bibliografia ##

* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite, wersja 3](https://www.loc.gov/preservation/digital/formats/fdd/fdd000461.shtml)

