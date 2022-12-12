{
  "date" : "2019-12-09",
  "keywords" :["plik zl", "format pliku zl", "co to jest plik zl", "plik", "przykład zl", "rozszerzenie pliku zl", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - Format skompresowanego pliku ZLIP",
  "description":"Poznaj format pliku ZL i interfejsy API, które mogą tworzyć i otwierać pliki ZL.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## Czym jest plik ZL?

Plik z rozszerzeniem .zl to skompresowany format pliku ZLIP, który wykorzystuje wariant algorytmu kompresji DEFLATE do kompresji plików. Jest niezależny od typu procesora, systemu operacyjnego, systemu plików i zestawu znaków, a zatem może być używany do wymiany informacji. Specyfikacje techniczne kompresji ZLIP są dostępne na stronie [IETF](https://tools.ietf.org/html/rfc1950) i można się do nich odnieść z perspektywy programisty.

## Format pliku ZL

Strumień zlib ma następującą strukturę:

* `CMF (Metoda kompresji i flagi)` - Ten bajt jest podzielony na 4-bitową metodę kompresji i 4-bitowe pole informacyjne w zależności od metody kompresji.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (metoda kompresji)` — identyfikuje metodę kompresji używaną w pliku. Jego wartości i odpowiednia metoda kompresji są następujące.

| Wartość CM| Kompresja|
|---|---|
|CM = 8|DEFLATE przy rozmiarze okna do 32K|
|CM = 15|Zarezerwowane|

* `CINFO (informacje o kompresji)` — dla CM = 8, CINFO jest logarytmem o podstawie 2 rozmiaru okna LZ77 minus osiem (CINFO=7 oznacza rozmiar okna 32K).

* `FLG (FLaGs)` - Ten bajt flagi jest podzielony w następujący sposób:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Bibliografia ##

* [Specyfikacje formatu plików Zlib](https://tools.ietf.org/html/rfc1950)

