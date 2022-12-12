{
  "date" : "2020-01-11",
  "keywords" :["plik x", "format pliku x", "co to jest plik x", "plik", "przykład x", "rozszerzenie pliku x", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - Format pliku DirectX 2.0",
  "description":"Dowiedz się o formacie plików DirectX X i interfejsach API, które mogą otwierać i tworzyć pliki DirectX X.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## Co to jest plik X?

Plik z rozszerzeniem .x odnosi się do [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) starszego formatu pliku grafiki 3D, który został wprowadzony wraz z Microsoft DirectX 2.0. Był używany do renderowania grafiki 3D w grach i określa struktury siatek, tekstur, animacji i obiektów zdefiniowanych przez użytkownika. Jest przestarzały od 2014 roku, ponieważ format pliku Autodesk FBX lepiej sprawdza się jako bardziej nowoczesny format. X jest oparty na szablonach i jest wolny od jakiejkolwiek wiedzy o użytkowaniu.

Możesz otwierać pliki DirectX X za pomocą Microsoft DirectX i popularnych edytorów tekstu.

## Format pliku X

[Odniesienie do pliku X](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) zawiera informacje referencyjne dotyczące elementów interfejsu API używanych do pracować z plikami DirectX .x. Format zapewnia prymitywy danych niskiego poziomu, które są używane przez inne aplikacje do definiowania prymitywów wyższego poziomu za pomocą szablonów danych. DirectX 6.0 wprowadził interfejsy i metody umożliwiające odczyt i zapis do plików .x. DirectX 3.0 wprowadził binarną wersję tego formatu plików.

[Odniesienie do formatu pliku X](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) zdefiniowane przez DirectX 9 zawiera informacje referencyjne dla .x pliki w kodowaniu binarnym i tekstowym.

### Kodowanie binarne

[Format binarny](https://docs.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) definiuje format DirectX X jako tokenizowaną reprezentację formatu tekstowego. Te tokeny mogą być samodzielne, aby nadać strukturę gramatyczną, lub mogą być tokenami zawierającymi rekordy, dostarczającymi niezbędnych danych.

#### Nagłówek

Nagłówek binarny można odczytywać i zapisywać przy użyciu następujących definicji.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Kodowanie tekstu

Pliki DirectX .x nie zależą od sposobu użycia pliku i nie są specyficzne dla żadnej aplikacji. To podejście oparte na szablonach umożliwia użycie formatu pliku .x przez dowolną aplikację kliencką.


#### Nagłówek

Nagłówek o zmiennej długości jest obowiązkowy i musi znajdować się na początku strumienia danych. Nagłówek zawiera następujące dane.

|Typ |Podtyp |Rozmiar |Zawartość |Zawartość Znaczenie|
---|---|---|---|---|
|Magiczna liczba (wymagane)| | 4 bajty |xz |
|Numer wersji (wymagany) |Numer główny |2 bajty |03 |Wersja główna 3|
| |Liczba podrzędna |2 bajty |02 |Wersja podrzędna 2|
|Typ formatu (wymagane)| |4 bajty |"txt " |Plik tekstowy|
| | | |"kosz"| Plik binarny|
| | | |"zip"| Skompresowany plik tekstowy MSZip|
| | | |"bzip"| Skompresowany plik binarny MSZip|
|Rozmiar zmiennoprzecinkowy (wymagany)| |4 bajty| 0064| 64-bitowe zmiennoprzecinkowe|
| | | |0032 |32-bitowe liczby zmiennoprzecinkowe|


## Bibliografia

* [Starsza wersja plików X](https://docs.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [Informacje o formacie plików DirectX 9](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

