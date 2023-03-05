{
  "date" : "2019-10-11",
  "keywords" :["plik bz2", "format pliku bz2", "co to jest plik bz2", "plik", "przykład bz2", "rozszerzenie pliku bz2", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - Format skompresowanego pliku",
  "description":"Dowiedz się, co to jest plik BZ2 i interfejsy API, które mogą tworzyć i otwierać pliki BZ2.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## Czym jest plik BZ2?

BZ2 to skompresowane pliki generowane przy użyciu metody kompresji open source [BZIP2](http://www.bzip.org/), głównie w systemie UNIX lub Linux. Służy do kompresji pojedynczego pliku i nie jest przeznaczony do archiwizacji wielu plików. Kontrastuje to z formatem plików TAR na tych samych platformach, który archiwizuje wiele plików w jednym pliku, ale bez kompresji. Pliki skompresowane jako BZ2 można rozpakować za pomocą aplikacji takich jak [WinZip](https://www.winzip.com/win/en/). BZIP2 używa algorytmu kompresji Run-Length Encoding (RLE) lub [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform), aby osiągnąć wysoki poziom kompresji.

## Format pliku BZ2

Dla tego formatu pliku nie są dostępne żadne formalne specyfikacje. Jednak nieoficjalne [specyfikacje poddane inżynierii wstecznej](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) pokazują, że strumień .bz2 składa się z 4-bajtowego nagłówka, po którym następuje przez zero lub więcej skompresowanych bloków. Bezpośrednio po nim następuje znacznik końca strumienia zawierający 32-bitowy CRC dla przetworzonego całego strumienia zwykłego tekstu. Pomiędzy skompresowanymi blokami nie ma wypełnienia, a wszystkie bloki są wyrównane bitowo.

## Rozpakuj/wyodrębnij plik BZ2

Możesz rozpakować plik BZ2 w systemach Windows i Mac OS za pomocą oprogramowania takiego jak WinZip. W systemie Linux następujące polecenie w terminalu.

```
bzip2 -d filename.bz2
```

## Bibliografia

* [Specyfikacje formatu BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

