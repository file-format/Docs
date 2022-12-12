{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku FMPSL i interfejsy API, które mogą tworzyć i otwierać pliki FMPSL.",
  "title" :"Format pliku FMPSL — plik łącza migawki FileMaker Pro 12",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## Czym jest plik FMPSL?

Plik FMPSL jest plikiem migawki bazy danych utworzonej za pomocą FileMaker Pro 12. Przechowuje wyniki zapytań z bazy danych wraz z innymi informacjami, takimi jak układ wizualny i widoczne informacje. Plik FMPSL może być użyty do przywrócenia wszystkich tych danych w innej instancji bazy danych FileMaker Pro. Ten format pliku został wprowadzony wraz z uruchomieniem FileMaker Pro v 12. Przed tą wersją łącza do migawek zostały wprowadzone jako format pliku FPSL w FileMaker Pro v 11. Pliki FMPSL można otwierać za pomocą oprogramowania FileMaker Pro Advanced. Inne formaty plików obsługiwane przez FileMaker Pro to [FP5](/pl/database/fp5/), [FP7](/pl/database/fp7/) i [FMP12](/pl/database/fmp12/).

## Format pliku FMPSL

Szczegóły wewnętrznego formatu plików FMPSL nie są publicznie dostępne w celach informacyjnych dla programistów.

### Jak zapisać rekordy jako plik FMPSL?

Dane z bazy danych FileMaker Pro można zapisać jako plik łącza migawki, wykonując następujące czynności.

1. Wyszukaj rekordy z bazy danych, które mają zostać zapisane jako plik łącza migawki.
1. Korzystając z opcji Wyślij rekord jako łącze do migawki z menu, zapisz plik, wprowadzając nazwę pliku.
1. Korzystając z przeglądanych Rekordów, zapisz cały znaleziony zestaw rekordów.

Wygenerowany plik migawki zostanie zapisany na dysku o określonej nazwie.

## Bibliografia

* [Konwertuj wcześniejsze wersje formatów plików FileMaker Pro do formatu plików FMP12](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [Zapisz rekordy jako plik łącza migawki](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

