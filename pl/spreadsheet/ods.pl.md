{
  "date" : "2019-12-10",
  "keywords" :["ODS", "plik", "rozszerzenie", "format pliku", "Arkusz kalkulacyjny OpenDocument" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Twój przewodnik po formatach plików, aby dowiedzieć się, co to jest plik ODS i interfejsy API, które mogą je tworzyć i otwierać.",
  "title" :"Co to jest plik ODS?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Czym jest plik ODS?

Pliki z rozszerzeniem .ods oznaczają format dokumentu arkusza kalkulacyjnego OpenDocument, który może być edytowany przez użytkownika. Dane są przechowywane w pliku ODF w wierszach i kolumnach. Jest to format oparty na XML i jest jednym z kilku podtypów w rodzinie Open Document Formats (ODF). Format jest określony jako część specyfikacji ODF 1.2 publikowanych i utrzymywanych przez OASIS. Wiele aplikacji w systemie Windows oraz innych systemach operacyjnych może otwierać pliki ODS do edycji i manipulacji, w tym Microsoft Excel, NeoOffice i LibreOffice. Pliki ODS można również konwertować na inne formaty arkuszy kalkulacyjnych, takie jak [XLS](/pl/spreadsheet/xls/), [XLSX](/pl/spreadsheet/xlsx/) i inne za pomocą różnych aplikacji.

## Krótka historia ##

Specyfikacje formatu plików ODS oparte są na standardzie opracowanym jako specyfikacje ODF. Te specyfikacje ewoluowały w przeszłości w postaci trzech wersji opracowanych i opublikowanych przez OASIS w następujący sposób:

`2005`- Wersja 1.0 została opublikowana w maju 2005

`2007` - Wersja 1.1 została opublikowana w lutym 2007

`2011` — wersja 1.2 została opublikowana we wrześniu 2011 r

Były dość drobne zmiany w przejściu z wersji ODF 1.0 do wersji 1.1. [Wersja ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) to najnowsza wersja specyfikacji ODF, z którą programiści powinni się konsultować w celu opracowania aplikacji związanych z odczytem/zapisem ODS.

## Format pliku ODS ##

Format OpenDocument obsługuje reprezentację dokumentów jako pojedynczy dokument XML, a także kolekcję kilku dokumentów podrzędnych w pakiecie jako archiwum [ZIP](/pl/compression/zip/). Każdy z plików z archiwum ZIP przechowuje część kompletnego dokumentu. Każdy dokument podrzędny przechowuje określony aspekt dokumentu. Na przykład jeden dokument podrzędny zawiera informacje o stylu, a inny dokument podrzędny zawiera treść dokumentu. Typowy dokument ODF składa się z następujących elementów:

* `content.xml` – Treść dokumentu i automatyczne style użyte w treści.
* `styles.xml` – Style używane w treści dokumentu i style automatyczne używane w samych stylach.
* `meta.xml` – metadane dokumentu, takie jak autor lub czas ostatniej akcji zapisu.
* `settings.xml` – Ustawienia specyficzne dla aplikacji, takie jak rozmiar okna lub informacje o drukarce.

Poza tym w pakiecie może znajdować się wiele innych dokumentów podrzędnych, takich jak miniatury dokumentów, obrazy itp.

Pliki dokumentów arkuszy kalkulacyjnych to podzbiór plików ODF, w których treść (arkusze) jest przechowywana w dokumencie podrzędnym content.xml.

## Bibliografia ##

* [OpenDocument – z Wikipedii](https://en.wikipedia.org/wiki/OpenDocument)

