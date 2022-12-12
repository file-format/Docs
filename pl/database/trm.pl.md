{
  "date" : "2022-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku TRM i interfejsy API, które mogą tworzyć i otwierać pliki TRM.",
  "title" :"Format pliku TRM - Plik mapy Oracle Trace",
  "linktitle" : "TRM",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Co to jest plik Oracle TRM?

Plik TRM to format pliku metadanych używany przez system zarządzania relacyjnymi bazami danych Oracle 11g (RDBMS). Jest przechowywany razem z plikami śledzenia Oracle ([.trc](/pl/database/trc/)) i zawiera informacje strukturalne dotyczące pliku śledzenia. Celem pliku TRM jest ułatwienie wyszukiwania i nawigacji po rekordach za pomocą informacji o metadanych. Oprogramowanie Oracle może być używane do otwierania plików TRM.

## Format pliku TRM

Pliki TRM są zapisywane w zastrzeżonym formacie plików Oracle, a szczegóły formatu plików TRM nie są publicznie dostępne. Typowy plik TRC zawiera identyfikator SID procesu Oracle, nazwę procesu i numer procesu systemu operacyjnego. Pliki TRM zawierają szczegółowe informacje o metadanych tych plików TRC do wyszukiwania i nawigacji.

## Bibliografia ##

* [Co to jest plik .trm w oracle 11g?](https://community.oracle.com/tech/developers/discussion/945615/what-is-trm-file-in-oracle-11g)

