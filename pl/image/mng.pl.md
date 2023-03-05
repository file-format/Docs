{
  "date" : "2019-10-11",
  "keywords" :[ "plik mng", "format pliku mng", "co to jest plik mng", "plik", "przykład mng", "rozszerzenie pliku mng", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku MNG — format pliku grafiki sieciowej z wieloma obrazami",
  "description":"Poznaj format pliku MNG i interfejsy API, które mogą tworzyć i otwierać pliki MNG.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik MNG?

Plik z rozszerzeniem .mng to format pliku Multi-image Network Graphics, który jest podobny do formatu obrazu [PNG](/pl/image/png/), ale obsługuje obrazy animowane. Został opracowany, aby uniknąć przeładowania formatu PNG dodatkową funkcją animacji. MNG jest również podobny do plików [GIF](/pl/image/gif/), ale wykorzystuje większą kompresję i obsługuje pełną funkcję alfa. Nieoficjalnym typem nośnika MIME dla plików MNG jest video/x-mng. Pliki MNG można otwierać w aplikacjach takich jak ImageMagik i IrfanView.

## Format pliku MNG

Format pliku MNG jest podobny do formatu PNG i wykorzystuje tę samą strukturę fragmentów, jak zdefiniowano w specyfikacjach PNG. Dekoder MNG musi być w stanie dekodować strumienie danych PNG bez określania żadnych specjalnych flag dla instrukcji dekodowania. MNG grupuje wiele obrazów razem w „ramkę”, przy czym niektóre obrazy są używane jako sprite do przemieszczania się z jednego miejsca do drugiego. Mechanizm pozwala na ponowne wykorzystanie danych obrazu bez ich retransmisji. [Specyfikacje MNG](http://www.libpng.org/pub/mng/spec/) można znaleźć w celach informacyjnych dla programistów.

### Podpis MNG

Strumień danych MNG zaczyna się od 8-bajtowej sygnatury zawierającej:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Jest to podobne do podpisu PNG, ale zawiera MNG zamiast PNG.

### Ramka MNG

Ramka MNG składa się z dwuwymiarowego obrazu mniejszych obrazów. Dostęp do każdego małego obrazu można uzyskać za pomocą kombinacji indeksu wiersza i kolumny. Format umożliwia przechowywanie trójwymiarowych danych „wokseli”, które są ułożone w szereg dwuwymiarowych płaszczyzn. Każda płaszczyzna jest reprezentowana przez strumień danych PNG lub Delta-PNG. Każdy strumień danych Delta-PNG definiuje obraz jako różnice w stosunku do nadrzędnego obrazu PNG. Zapewnia to znacznie bardziej zwarty sposób przedstawiania kolejnych obrazów niż użycie pełnego strumienia danych PNG dla każdego z nich.

## Bibliografia ##

* [MNG](http://www.libpng.org/pub/mng/)
* [Format MNG v 1.0](http://www.libpng.org/pub/mng/spec/)

