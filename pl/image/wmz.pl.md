{
  "date" : "2019-10-11",
  "keywords" :[ "plik wmz", "format pliku wmz", "co to jest plik wmz", "plik", "przykład wmz", "rozszerzenie pliku wmz", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku WMZ — skompresowany metaplik systemu Windows",
  "description":"Poznaj format pliku WMZ i interfejsy API, które mogą tworzyć i otwierać pliki WMZ.",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Czym jest plik WMZ?

Plik z rozszerzeniem .wmz jest skompresowaną wersją [WMF](/pl/image/wmf/) i służy do przechowywania metaplików. Jest to plik poziomu pośredniego generowany przez starsze wersje aplikacji Microsoft Office i nie jest zbyt popularnie używany. Pliki WMZ są generowane podczas zapisywania dokumentów w formacie [HTML](/pl/web/html/). Mogą one być również generowane podczas wysyłania pocztą e-mail dokumentów zawierających osadzone obiekty clipart, równania itp. Aplikacje, które mogą otwierać pliki WMZ, obejmują między innymi Corel Winzip i Apple Archive Utility.

## Format pliku WMZ

Pliki WMZ są skompresowane [Gzip](/pl/compression/gz/) i zawierają [WMF](/pl/image/WMF/). Gzip używa algorytmu DEFLATE do kompresji archiwum. GZIP różni się od formatu archiwum [ZIP](/pl/compression/zip/), ponieważ stosuje algorytm kompresji do całego archiwum, a nie do poszczególnych plików. Format pliku składa się z:

* Nagłówek pliku
* Opcjonalne nagłówki
* Skompresowane dane
* Stopka pliku

Format pliku GZIP [wersja specyfikacji 4.3](https://datatracker.ietf.org/doc/html/rfc1952) opublikowany przez Internet Engineering Task Force (IETF) zawiera szczegółowe informacje o formacie pliku.

## Bibliografia

* [RFC1952: specyfikacja formatu pliku GZIP](https://datatracker.ietf.org/doc/html/rfc1952), przez [IETF](https://www.ietf.org)
* [Metaplik systemu Windows – Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

