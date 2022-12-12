{
  "date" : "2019-10-11",
  "keywords" :[ "ixbrl","plik ixbrl", "format pliku ixbrl", "typ pliku ixbrl", "plik", "typ", "co to jest plik ixbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IXBRL – format pliku sprawozdawczości biznesowej i finansowej",
  "description":"Poznaj format pliku IXBRL i interfejsy API, które mogą tworzyć i otwierać pliki IXBRL.",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Czym jest plik iXBRL?

Format pliku iXBRL (ilnine XBRL) umożliwia osadzenie danych [XBRL](/pl/web/xbrl/) w pliku HTML, aby był on czytelny zarówno dla maszyny, jak i dla człowieka. W rzeczywistości jest to plik [xHTML](/pl/web/xhtml/), który wykorzystuje znaczniki XBRL i został opracowany przez XBRL International w celu spełnienia wymagań brytyjskiego HMRC. Za pomocą iXBRL można tworzyć sprawozdania finansowe, zachowując nienaruszony układ oryginalnego dokumentu. Pliki iXBRL można otwierać w dowolnym edytorze tekstu, takim jak Notatnik w systemie operacyjnym Windows i TextEdit w systemie MacOS.

## Format pliku iXBRL

Wewnątrz iXBRL zawartość XBRL jest opakowana w plik w formacie xHTML, który wykorzystuje znaczniki XML. jak XBRL,<xbrl> jest elementem głównym plików iXBRL. Format XHTML przedstawia swoją zawartość jako zbiór różnych typów dokumentów i modułów. Wszystkie pliki w XHTML są oparte na formacie plików XML i są zgodne ze standardami dokumentów XML. XHTML jest formatem niezbędnym do operacyjnego wykorzystania zależnego [HTML](/pl/web/html/) Document Object Model (DOM) lub [XML](/pl/web/xml/) Document Object Model. W świecie zewnętrznym iXBRL jest zgodny ze specyfikacjami formatu plików [xHTML](/pl/web/xhtml/).

### iXBRL kontra XBRL

XBRL można porównać do iXBRL na podstawie następujących czynników:

* Złożoność
* Opcje formatowania
* Typy plików/rozszerzenia
* Opcja renderowania
* Proces składania

Poniższa tabela ilustruje te różnice.

|Parametr|XBRL|iXBRL|
---|---|---|
|Złożoność|Bardziej złożony niż iXBRL|Mniej złożony ze względu na istniejący schemat organizacyjny XHTML|
|Opcje formatowania|Ograniczona elastyczność|Wysoka elastyczność formatowania treści|
|Typy plików/rozszerzenia|Formalnie zapisywane z rozszerzeniem .xml|Zwykle zapisywane jako rozszerzenie .html lub .xhtml|
|Opcje renderowania|Do przeglądania tych treści wymagane są przeglądarki XBRL|Treść czytelna dla człowieka, którą można przeglądać w przeglądarkach|
|Proces archiwizacji| Dokumenty instancji XBRL (do odczytu maszynowego) i HTML (do odczytu przez człowieka) należy przechowywać oddzielnie.|W jednym dokumencie dostępne są zarówno formaty czytelne dla ludzi, jak i dla maszyn.|

## Bibliografia

* [XBRL – z Wikipedii](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)

