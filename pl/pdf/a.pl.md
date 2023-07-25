{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku PDF/A",
  "description":"Poznaj format pliku PDF/A i interfejsy API, które mogą tworzyć i otwierać pliki PDF/A.",
  "linktitle" : "PDF/A",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Co to jest PDF/A? #

PDF/A to standardowy format ISO służący do archiwizacji dokumentów elektronicznych w formacie PDF. Głównym celem jego powstania było spełnienie wymagań długoterminowej archiwizacji. Norma zapewnia otwieranie zarchiwizowanych plików nawet po długim czasie, nakładając pewne ograniczenia na integralne części dokumentu w celu osiągnięcia zgodności. Format ten jest obecnie szeroko stosowany we wszystkich branżach. Przeglądarki PDFA/A, takie jak Adobe Acrobat Reader, zapewniają, że pliki zapisane w tym formacie będą mogły być otwierane nawet w przyszłości, zgodnie z informacjami udostępnianymi przez ten standard.

## Wersje PDF/A ##

PDF/A został przyjęty jako standard ISO w październiku 2005 roku. Od tego czasu jest stale ulepszany, az biegiem czasu opracowano kilka kolejnych standardów. Informacje o publikowanych wraz z upływem czasu standardach PDF/A oraz ich szczegóły przedstawiają się następująco:

* **PDF/A-1:** opublikowany w październiku 2005 jako ISO 19005-1 i oparty na PDF 1.4
* **PDF/A-2:** opublikowany w czerwcu 2011 r. jako ISO 19005-2 i oparty na PDF 1.7 (ISO 32000-1:2008)
* **PDF/A-3:** opublikowany w październiku 2012 r. jako ISO 19005-3 i oparty na PDF 1.7 (ISO 32000-1:2008)

## PDF/A-1 ##

Standard PDF/A-1 został oparty na oryginalnej wersji PDF 1.4. Standard PDF/A-1 definiuje dwa poziomy zgodności dla plików PDF.

### PDF/A-1a ###

Jest zgodny z poziomem A i spełnia wszystkie wymagania specyfikacji standardu PDF/A-1. PDF/A-1a zapewnia, że tekst można wyodrębnić z dokumentu. Gwarantuje również, że naturalny proces czytania zintegrowanego materiału tekstowego pozostanie nienaruszony. PDF/A nakłada wymóg zdolności reprezentacji tekstu na zmniejszonych ekranach poprzez restrukturyzację, która jest znana jako „tagowany PDF”. Miało to na celu zwiększenie dostępności zgodnych plików dla użytkowników z upośledzeniem fizycznym poprzez umożliwienie oprogramowania wspomagającego.

### PDF/A-1b ###

PDF/A-1b to niższy poziom zgodności i dotyczy wyglądu dokumentów elektronicznych w stosunku do normy ISO 19005. Zapewnia równomierne odtwarzanie tekstu i innych treści na stronach. Ta zgodność na poziomie B wskazuje na minimalną zgodność, aby zapewnić, że renderowany wygląd zgodnego pliku będzie można zachować w dłuższej perspektywie.

## PDF/A-2 ##

PDF/A-2 został wydany przez ISO Standard w lipcu 2011 jako nowy standard znany jako ISO 32001-1. Ten nowy standard nie tylko korzystał ze wszystkich funkcji wersji PDF do wersji 1.7, ale został również wprowadzony jako nowy standard. PDF/A-2 zawierał następujące funkcje jako część tego nowego standardu.

* PDF/A-2 jest dostarczany z obsługą formatu [JPEG2000](/pl/image/jp2/), który jest pomocny w przypadku zeskanowanych dokumentów.
* Obsługuje osadzanie kolekcji PDF/A, których można użyć do utworzenia kontenera PDF zawierającego inne podobne pliki
* Obsługuje funkcję przezroczystości plików PDF w całości w porównaniu z PDF/A-1, gdzie była częściowo obsługiwana.
* PDF/A-2 zapewnia obsługę opcjonalnych treści przydatnych do mapowania aplikacji i rysunków technicznych. Są one również znane jako warstwy, które mogą być widoczne lub ukryte zgodnie z wymaganiami osoby oglądającej.
* Określa wymagania dotyczące niestandardowych metadanych XMP
* Dodaje niektóre nowsze typy komentarzy do listy zabronionych typów adnotacji. Ponadto do listy akceptowanych elementów dodano niektóre nowsze typy komentarzy, takie jak komentarze dotyczące edycji tekstu.

## PDF/A-3 ##

PDF/A-3 zawiera wszystkie wymagania zgodności poziomu 2 i umożliwia osadzanie dodatkowych formatów plików (takich jak XML, [CSV](/pl/spreadsheet/csv/), [CAD](/pl/cad/), [przetwarzanie tekstu](/pl/przetwarzanie tekstu/) , [arkusz kalkulacyjny](/pl/arkusz kalkulacyjny/) i inne) na dokumenty zgodne z formatem PDF/A.

## Bibliografia ##

* [PDF/A – z Wikipedii](https://en.wikipedia.org/wiki/PDF/A)
* [Biała księga: PDF/A – podstawy](https://www.pdf-tools.com/public/downloads/whitepapers/whitepaper-pdfa.pdf)

