{
  "date" : "2019-10-11",
  "keywords" :[ "plik odp", "format pliku odp", "co to jest plik odp", "plik", "przykład odp", "rozszerzenie pliku odp", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP — format pliku prezentacji OpenOffice",
  "description":"Poznaj format plików ODP i interfejsy API, które mogą tworzyć i otwierać pliki ODP.",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik ODP?

Pliki z rozszerzeniem .odp reprezentują format pliku prezentacji używany przez OpenOffice.org w standardzie OASISOpen. Plik prezentacji to zbiór slajdów, z których każdy może zawierać tekst, obrazy, formatowanie, animacje i inne multimedia. Slajdy te są prezentowane publiczności w formie pokazów slajdów z niestandardowymi ustawieniami prezentacji. Pliki ODP mogą być otwierane przez aplikacje zgodne z formatem OpenDocument (takie jak OpenOffice lub StarOffice).

## Krótka historia

Specyfikacje formatu plików ODP oparte są na standardzie opracowanym jako specyfikacje ODF. Te specyfikacje ewoluowały w przeszłości w postaci trzech wersji opracowanych i opublikowanych przez OASIS w następujący sposób:

`2005` - Wersja 1.0 została opublikowana w maju 2005
`2007` - Wersja 1.1 została opublikowana w lutym 2007
`2011` — wersja 1.2 została opublikowana we wrześniu 2011 r

Były dość drobne zmiany w przejściu z wersji ODF 1.0 do wersji 1.1. [Wersja ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) to najnowsza wersja specyfikacji ODF, z którą programiści powinni się konsultować w celu opracowania aplikacji związanych z odczytem/zapisem ODS.

## Specyfikacje formatu plików

Format OpenDocument obsługuje reprezentację dokumentów jako pojedynczy dokument XML, a także kolekcję kilku dokumentów podrzędnych w pakiecie jako archiwum [ZIP](https://docs.fileformat.com/compression/zip/). Każdy z plików z archiwum ZIP przechowuje część kompletnego dokumentu. Każdy dokument podrzędny przechowuje określony aspekt dokumentu. Na przykład jeden dokument podrzędny zawiera informacje o stylu, a inny dokument podrzędny zawiera treść dokumentu. Typowy dokument ODF składa się z następujących elementów:

* `content.xml` – Treść dokumentu i automatyczne style użyte w treści.
* `styles.xml` – Style używane w treści dokumentu i style automatyczne używane w samych stylach.
* `meta.xml` – metadane dokumentu, takie jak autor lub czas ostatniej akcji zapisu.
* `settings.xml` – Ustawienia specyficzne dla aplikacji, takie jak rozmiar okna lub informacje o drukarce.

Poza tym w pakiecie może znajdować się wiele innych dokumentów podrzędnych, takich jak miniatury dokumentów, obrazy itp.

Pliki dokumentów arkusza kalkulacyjnego są podzbiorem plików ODF, w których zawartość (arkusze) jest przechowywana w dokumencie podrzędnym content.xml.

## Bibliografia

* [OpenDocument – z Wikipedii](https://en.wikipedia.org/wiki/OpenDocument)

