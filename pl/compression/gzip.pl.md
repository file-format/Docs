{
  "date" : "2022-06-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku GZIP - Spakowany plik archiwum GNU",
  "description":"Dowiedz się, co to jest plik GZIP i interfejsy API, które mogą tworzyć i otwierać pliki GZIP.",
  "linktitle" : "GZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-26"
}

## Czym jest plik GZIP?

Plik GZIP to skompresowane archiwum utworzone przy użyciu standardowego algorytmu kompresji [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Skompresowane archiwum może zawierać wiele plików, w tym pliki skompresowane, katalogi i kody pośredniczące plików. Większość systemów Unix zawiera narzędzie do kompresji gzip (GNU Zip) o otwartym kodzie źródłowym do kompresji/dekompresji plików. Pliki GZIP można otwierać za pomocą aplikacji takich jak [WinZip](https://www.winzip.com/en/).

## Format pliku GZIP — więcej informacji

GZIP używa algorytmu [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) do kompresji plików do archiwów. Dwa dokumenty RFC, [RFC1952](https://tools.ietf.org/html/rfc1952) i [RFC 1951](https://tools.ietf.org/html/rfc1951), określają specyfikację formatu opakowania gzip i odpowiednio opróżniać skompresowany format danych.

Pliki GZIP są często zapisywane w formacie [GZ](/pl/compression/gz/).

## Bibliografia

* [gzip](http://www.gzip.org/)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: specyfikacja formatu pliku GZIP](https://datatracker.ietf.org/doc/html/rfc1952), przez IETF
* [RFC 1951](https://tools.ietf.org/html/rfc1951)

