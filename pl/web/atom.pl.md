{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik ATOM - format syndykacji Atom",
  "description" :"Dowiedz się, co to jest plik ATOM i interfejsy API, które mogą tworzyć i otwierać pliki ATOM.",
  "linktitle" : "ATOM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Czym jest plik ATOM?

Plik ATOM to format syndykacji dla struktury kanałów informacyjnych Atom i dokumentów wejściowych. Podobnie jak pliki .RSS, format pliku ATOM to oparty na XML format syndykacji, który jest standardem publikowania treści. Plik ATOM jest używany do kanałów internetowych, które umożliwiają programom sprawdzanie aktualizacji publikowanych na stronie internetowej. Zawiera wpisy, które mogą być różnego typu, takie jak nagłówki, pełne teksty artykułów, fragmenty lub linki do treści na stronie internetowej

Aplikacje, które mogą **otwierać pliki ATOM**, to **Apple Safari**.

## Format pliku ATOM — więcej informacji

Pliki ATOM są przechowywane i publikowane w popularnym formacie pliku XML, który jest uniwersalnym formatem wymiany informacji. Został opracowany jako alternatywa dla RSS, mając na uwadze ograniczenia i wady formatu plików RSS.

### Typy dokumentów Atomu

1. „Dokumenty wejścia Atom” — jest to dokument XML, który składa się z pojedynczej pozycji informacji, zwanej wpisem, dla kanału informacyjnego Atom. ma atom:entry element zawierający pewną liczbę elementów podrzędnych. Treść wpisu Atom może być zwykłym tekstem, HTML, XHTML lub innym typem nośnika IANA (Internet Assigned Numbers Authority).
1. „Dokumenty kanału Atom” — jest to dokument XML zawierający metadane dotyczące kanału Atom oraz jeden lub więcej wpisów dotyczących kanału. Gdy klient żąda informacji z kanału, serwer generuje dokument kanału, który zawiera pewną liczbę wpisów Atom, aby spełnić żądanie.
1. `Atom Collection` - Jest to specjalny rodzaj dokumentu kanału Atom, który zawiera adresy URL wpisów Atom, które można edytować.

## Bibliografia

* [Format syndykacji Atom — RFC](https://www.rfc-editor.org/rfc/rfc4287.html)
* [Przegląd kanałów Atom — IBM](https://www.ibm.com/docs/en/cics-ts/5.4?topic=support-overview-atom-feeds)
* [Atom - standard internetowy](https://en.wikipedia.org/wiki/Atom_(web_standard))

