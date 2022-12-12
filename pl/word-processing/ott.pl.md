{
  "date" : "2019-10-11",
  "keywords" :[ "plik ott", "format pliku ott", "co to jest plik ott", "plik", "przykład ott", "rozszerzenie pliku ott", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTT - plik szablonu OpenDocument",
  "description":"Poznaj format pliku OTT i interfejsy API, które mogą tworzyć i otwierać pliki OTT.",
  "linktitle" : "OTT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik OTT?

Pliki z rozszerzeniem OTT reprezentują szablony dokumentów generowane przez aplikacje zgodnie ze standardowym formatem OpenDocument firmy OASIS. Są one tworzone za pomocą aplikacji edytora tekstu, takich jak bezpłatny OpenOffice Writer, i mogą zawierać ustawienia, których można użyć do generowania nowych dokumentów z tych plików szablonów. Te ustawienia obejmują marginesy strony, obramowania, nagłówki, stopki i inne ustawienia strony. Takie szablony są używane w oficjalnych dokumentach, takich jak firmowy papier firmowy i standardowe formularze.

## Krótka historia ##

Specyfikacje formatu plików ODP oparte są na standardzie opracowanym jako specyfikacje ODF. Te specyfikacje ewoluowały w przeszłości w postaci trzech wersji opracowanych i opublikowanych przez OASIS w następujący sposób:

**2005:** Wersja 1.0 została opublikowana w maju 2005

**2007:** Wersja 1.1 została opublikowana w lutym 2007

**2011:** Wersja 1.2 została opublikowana we wrześniu 2011 r

Były dość drobne zmiany w przejściu z wersji ODF 1.0 do wersji 1.1. [Wersja ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) to najnowsza wersja specyfikacji ODF, z którą programiści powinni się konsultować w celu opracowania aplikacji związanych z odczytem/zapisem ODS.

## Specyfikacje formatu plików

Format OpenDocument obsługuje reprezentację dokumentów jako pojedynczy dokument XML, a także kolekcję kilku dokumentów podrzędnych w pakiecie jako archiwum [ZIP](/pl/Compression/ZIP/). Każdy z plików z archiwum ZIP przechowuje część kompletnego dokumentu. Każdy dokument podrzędny przechowuje określony aspekt dokumentu. Na przykład jeden dokument podrzędny zawiera informacje o stylu, a inny dokument podrzędny zawiera treść dokumentu. Typowy dokument ODF składa się z następujących elementów:

* content.xml – Zawartość dokumentu i automatyczne style użyte w treści.
* styles.xml – Style używane w treści dokumentu i style automatyczne używane w samych stylach.
* meta.xml — metadane dokumentu, takie jak autor lub czas ostatniej akcji zapisu.
* settings.xml — Ustawienia specyficzne dla aplikacji, takie jak rozmiar okna lub informacje o drukarce.

Poza tym w pakiecie może znajdować się wiele innych dokumentów podrzędnych, takich jak miniatury dokumentów, obrazy itp. Pliki dokumentów to podzbiór plików ODF, w których zawartość (arkusze) jest przechowywana w //content.xml//dokument podrzędny.

## Bibliografia ##

* [OpenDocument – z Wikipedii](https://en.wikipedia.org/wiki/OpenDocument)

