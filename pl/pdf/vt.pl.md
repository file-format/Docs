{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku PDF/VT",
  "description":"Poznaj format plików PDF/VT i API, które mogą tworzyć i otwierać pliki PDF/VT.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Co to jest PDF/VT? #

PDF/VT, opublikowany jako [ISO 16612-2](https://www.iso.org/standard/46428.html) w sierpniu 2010 jako standard, ma na celu umożliwienie drukowania dokumentów zmiennych (VDP) w różnych środowiska. Standard sprawia, że podstawą dla standardu są informacje zmienne i drukowanie transakcyjne. Druk danych zmiennych stosuje się tam, gdzie część informacji jest inna dla każdego odbiorcy treści. Druk transakcyjny obejmuje faktury, wyciągi i inne dokumenty, które łączą informacje rozliczeniowe z informacjami marketingowymi. Powoduje to połączenie ulepszonego przetwarzania obrazów, tekstu i innych typów treści. PDF/VT umożliwia niezawodne i dynamiczne zarządzanie stronami w przypadku danych drukowania High Volume Transactional Output (HVTO) przy użyciu koncepcji metadanych części dokumentu (DPM). Pliki PDF/VT można otwierać w przeglądarce Adobe Acrobat bez konieczności dodawania jakiegokolwiek innego komponentu.

## Hierarchia części dokumentu ##

Hierarchia części dokumentu (DPart) przypomina strukturę drzewa węzłów części dokumentu opartą na wszystkich stronach dokumentu. Elementy tego drzewa nazywane są węzłami DPart. Każdy węzeł wewnętrzny zawiera inne węzły DPart, a każdy węzeł-liść określa jedną lub więcej stron dla odbiorcy. Zasadniczo hierarchia DPart określa kolejność i relacje między dokumentami lub fragmentami dokumentów w pliku PDF/VT. Struktura drzewiasta węzłów DPart łatwo przedstawia wewnętrzną zawartość dokumentu PDF/VT, ponieważ może zawierać dokumenty podrzędne dla wielu odbiorców, a każda część dokumentu odpowiada stronom dla jednego odbiorcy. Hierarchia DPart jest wymagana w plikach PDF/VT.

## Metadane części dokumentu (DPM) ##

Metadane części dokumentu (DPM) są powiązane z każdym węzłem w hierarchii części dokumentu i mogą służyć do przekazywania informacji o dokumencie podrzędnym określonego odbiorcy i jego częściach. W szczególności DPM może zawierać informacje o właściwościach lub informacje o odbiorcach w postaci zakodowanej.

## Poziomy zgodności ##

PDF/VT jest przyznawany na następujących trzech poziomach zgodności. Wszystkie są oparte na [PDF](/pl/pdf/) 1.6.

* `PDF/VT-1` — jest oparty na PDF/X-4 i zawiera wszystkie zasoby wymagane do renderowania dokumentu PDF.
* `PDF/VT-2` — zaprojektowane do wymiany wielu plików, dokumenty PDF/VT-2 mogą odnosić się do zewnętrznych zamiarów wyjściowych, zewnętrznych treści lub obu. Dokument PDF/VT i wszystkie powiązane z nim pliki PDF oraz zewnętrzne zamiary wyjściowe są zbiorczo nazywane zestawem plików PDF/VT-2. Acrobat 9 i obsługuje tę funkcję.
* `PDF/VT-2s` — obsługuje przesyłanie strumieniowe na żywo w formacie PDF/VT-2. Pozwala to na przetwarzanie segmentowanych sekcji danych.

## Bibliografia ##

* [PDF/VT – z Wikipedii](https://en.wikipedia.org/wiki/PDF/VT)
* [Technologia graficzna ISO 16612-2](https://www.iso.org/standard/46428.html)

