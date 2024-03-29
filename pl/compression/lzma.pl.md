{
  "date" : "2021-04-08",
  "keywords" :[ "plik lzma", "format pliku lzma", "co to jest plik lzma", "plik", "przykład lzma", "rozszerzenie pliku lzma", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - Format skompresowanego pliku LZMA",
  "description":"Co to jest plik LZMA i interfejsy API, które mogą tworzyć i otwierać pliki LZMA.",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## Czym jest plik LZMA?

Plik z rozszerzeniem .lzma to skompresowany plik archiwum utworzony przy użyciu metody kompresji LZMA (Lempel-Ziv-Markov chain Algorithm). Można je znaleźć/używać głównie w systemie operacyjnym Unix i są one podobne do innych algorytmów kompresji, takich jak [ZIP](/pl/compression/zip/) w celu minimalizacji rozmiaru pliku. LZMA to starszy format pliku, który jest lub został zastąpiony formatem .xz. Typ MIME formatu .lzma to \`application/x-lzma'. Ten format pliku został zaprojektowany przez Igora Pavlova do użytku w LZMA SDK.

## Format pliku LZMA

Plik LZMA składa się z dwóch głównych części:

1. Nagłówek
1. Skompresowane dane


### Nagłówek LZMA

Pliki LZMA mają 13-bajtowy nagłówek, po którym następują skompresowane dane LZMA. Nagłówek LZMA składa się z:

* Nieruchomości
* Rozmiar słownika
* Rozmiar nieskompresowany

#### Właściwości nagłówka LZMA

Pole Właściwości zawiera trzy właściwości. W nawiasie podany jest skrót, po którym następuje zakres wartości właściwości. Pole składa się z

1) liczba bitów kontekstu literalnego (lc, [0, 8]);
2) liczba bitów pozycji literalnej (lp, [0, 4]); oraz
3) liczba bitów pozycji (pb, [0, 4]).

#### Rozmiar słownika LZMA

Jest to przechowywane jako 32-bitowa liczba całkowita little endian bez znaku z wartościami z zakresu od 2^n do 2^n + 2^(n-1). LZMA Utils może dekompresować pliki o dowolnym rozmiarze słownika.

#### Nieskompresowany rozmiar
Rozmiar po nieskompresowaniu jest przechowywany jako 64-bitowa liczba całkowita little endian bez znaku. Specjalna wartość 0xFFFF_FFFF_FFFF_FFFF wskazuje, że nieskompresowany rozmiar jest nieznany. Wartość jest reprezentowana przez znacznik końca ładunku (\*) wtedy i tylko wtedy, gdy rozmiar nieskompresowanego jest nieznany.

## Bibliografia

* [Algorytm łańcucha Lempela-Ziva-Markowa](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)
