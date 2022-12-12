{
  "date" : "2019-10-11",
  "keywords" :["plik żywności", "format pliku żywności", "co to jest plik żywności", "plik", "przykład żywności", "rozszerzenie pliku żywności", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - Format pliku rysunku OpenDocument",
  "description":"Poznaj format pliku FODG i interfejsy API, które mogą tworzyć i otwierać pliki FODG.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik FODG?

Plik z rozszerzeniem .fodg to format pliku rysunku Apache OpenOffice do przechowywania elementów rysunkowych. Opiera się na specyfikacjach formatu plików określonych przez Advancement of Structural Information Standards (OASIS). Innym podobnym formatem pliku grafiki OpenOffice jest [ODG](/pl/image/odg/), który przechowuje elementy rysunkowe jako obraz wektorowy. Pliki FODG można otwierać za pomocą OpenOffice oraz LibreOffice. Inne formaty plików obsługiwane przez OpenOffice to na przykład [ODT](/pl/przetwarzanie tekstu/odt/), ODF, [ODP](/pl/presentation/odp/) i [ODS](/pl/spreadsheet/ods/).

## Format pliku FODG

FODG jest oparty na formacie pliku XML OpenDocument, który jest zgodny z formatem OASIS OpenDocument ISO/IEC 26300. Ma aplikację Internet Media Type/vnd.oasis.opendocument.graphics, a także jest zgodny z org.oasis-open.opendocument public.composite-content . Struktura XML jest wspólna dla wszystkich typów dokumentów, takich jak arkusze kalkulacyjne, pliki rysunków i dokumenty tekstowe. Dokumenty OpenOffice wykorzystują separację problemów, oddzielając zawartość, style, metadane i ustawienia aplikacji w czterech oddzielnych plikach XML.

`<office:document-content> ` - Treść dokumentu i automatyczne style użyte w treści.
`<office:document-styles> ` - Style używane w treści dokumentu i style automatyczne używane w samych stylach.
`<office:document-meta> ` — metadane dokumentu, takie jak autor lub czas ostatniej operacji zapisu.
`<office:document-settings> ` - Ustawienia specyficzne dla aplikacji, takie jak rozmiar okna lub informacje o drukarce.

## Bibliografia ##
* [Przyszłe specyfikacje standaryzacji w wersji 1.3 ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [Format otwartego dokumentu OASIS dla aplikacji biurowych](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Format OpenDocument – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

