{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - plik szablonu raportu Elixir",
  "description":"Poznaj plik RML i interfejsy API, które mogą tworzyć i otwierać pliki RML.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Czym jest plik RML?

Plik RML to plik szablonu raportowania z mechanizmem raportowania [Elixir Repertoire](https://elixirtech.com/repertoire-2/). Plik szablonu służy do generowania raportów ze źródłem danych podłączonym do systemu plików Elixir. Dane są odczytywane i wypełniane w pliku szablonu RML i mogą być eksportowane do wielu różnych formatów plików, takich jak [PDF](/pl/pdf/), [RTF](/pl/przetwarzanie tekstu/rtf/) i arkusz kalkulacyjny [XLS] (/pl/arkusz kalkulacyjny/xls/). Mechanizm raportowania Elixir Repertoire można połączyć z szeroką gamą źródeł danych JDBC.

## Format pliku RML

Szczegóły wewnętrznej struktury plików formatu pliku RML nie są publicznie dostępne. Pliki są generowane i zapisywane wewnętrznie przez aplikację Elixir Repertoire w celu generowania raportów z danymi wypełnionymi z podłączonych źródeł danych. Plik szablonu RML zawiera ogólny układ i informacje zastępcze raportu końcowego, który ma zostać wygenerowany z danych.

## Jak plik szablonu RML?

W celu wygenerowania szablonu RML w Elixir Repertoire można wykonać następujące kroki.

1. Podłącz źródło danych JDBC do systemu plików.
1. Uruchom Kreatora szablonów raportów
1. Użyj oprogramowania, aby zlokalizować plik .ds źródła danych
1. Wybierz raport tabelaryczny jako eksport
1. Wybierz pola, które mają zostać uwzględnione w szablonie raportu
1. Na koniec, po kliknięciu przycisku Zakończ, pierwszy raport.rml jest dodawany do repozytorium i otwierany w celu wyświetlenia zakładki Układ.

## Bibliografia

* [Repertuar eliksirów](https://elixirtech.com/repertoire-2/)

