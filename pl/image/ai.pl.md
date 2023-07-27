{
  "date" : "2021-01-21",
  "keywords" :[ "plik ai", "format pliku ai", "co to jest plik ai", "plik", "przykład ai", "rozszerzenie pliku ai", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI — plik graficzny programu Adobe Illustrator",
  "description":"Poznaj format plików AI i interfejsy API, które mogą tworzyć i otwierać pliki AI.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## Czym jest plik AI?

Plik z rozszerzeniem .ai to plik Adobe Illustrator Artwork, który zawiera grafikę wektorową na jednej stronie. używa punktów do tworzenia ścieżek do wyświetlania danych obrazu, chroniąc go w ten sposób przed utratą jakości obrazu w przypadku powiększenia. Format pliku AI jest oparty na formacie pliku PGF, który jest podobny do plików AI. Format AI znajduje swoje główne zastosowanie w przypadku logo i mediów drukowanych, a jego początkowe wersje uznano za podobne do plików [EPS](/pl/page-description-language/eps/). Pliki AI można otwierać za pomocą narzędzi Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro i CorelDraw Graphics.

## Format pliku AI

AI jest zastrzeżonym formatem plików programu Adobe Illustrator i wykorzystuje podejście podwójnej ścieżki podobne do PGF do zapisywania plików zgodnych z EPS. [Specyfikacje formatu plików programu Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) zawierają szczegółowe informacje dla programistów dotyczące wewnętrznych szczegółów tego formatu pliku. Wszystkie Dokumenty (pliki) tworzone przez Adobe Illustrator są dokumentami języka PostScript i składają się z dwóch głównych części zgodnych z Konwencjami strukturyzowania dokumentów: `prolog` i `script`.

### Prolog

Sekcja prologu zawiera informacje wymagane do interpretacji pliku. Przykładem może być obwiednia zawierająca wszystkie znaczniki na stronie. Zawiera również informacje o zasobach, takie jak czcionki i definicje procedur. Zasoby te są logicznie pogrupowane w zestawy zwane procsetami i zawierają jawne metody inicjowania i kończenia swoich procedur.

### Skrypt

Elementy graficzne na stronie są opisane przez skrypt. Skrypt zawiera odniesienia do operatorów i procedur w prologu, wraz z operandami i danymi. Trzy logiczne sekcje skryptu obejmują:

* Sekwencja instalacji - która inicjuje i aktywuje zasoby zdefiniowane w prologu
* Sekwencja operatorów opisowych
* Zwiastun, który dezaktywuje zasoby

Operatory w skrypcie to sekwencje elementów graficznych napisane w języku zdefiniowanym przez procsets w prologu. Sekwencje te składają się z kolekcji elementów danych, definicji atrybutów graficznych i wywołań procedur zdefiniowanych w plikach procsets.

### Znaczniki obiektów

Znaczniki obiektów służą do dołączania niestandardowych informacji do obiektów graficznych programu Adobe Illustrator. Tagi składają się z:

* Identyfikator znacznika
* Typ znacznika
* Dane

## Bibliografia
* [Specyfikacje formatu plików Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [Format pliku AI firmy PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)

