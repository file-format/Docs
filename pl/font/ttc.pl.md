{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC — format pliku kolekcji TrueType",
  "description":"Plik TrueType Collection (TTC) łączy wiele czcionek w jeden plik. Zarówno Apple, jak i Microsoft używały TTF w systemach operacyjnych Mac i Windows.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Czym jest plik TTC?
TTC jest określany skrótem TrueType Collection, który jest rozszerzeniem formatu True Type. Plik TTC może łączyć w sobie wiele plików czcionek. Pliki te są przydatne do łączenia wielu czcionek, które mają wiele wspólnych glifów. Przed Windows 2000 pliki TTC były używane w chińskich, japońskich i koreańskich wersjach systemu Windows, ale później obsługa była dostępna dla wszystkich regionów.


## Struktura pliku kolekcji czcionek
Plik TTC składa się z tabeli nagłówków TTC, katalogów tabel i wielu tabel OpenType. Nagłówek TTC musi znajdować się na początku pliku. Musi istnieć pełny katalog tabeli dla każdej czcionki. Format TableDirectory powinien być podobny do istniejącego w pliku niezbiorczym. Liczniki tabel we wszystkich katalogach w pliku TTC są obliczane od początku pliku TTC.
Tabele w pliku TTC są przywoływane przez katalog tabel odpowiadających im czcionek. Kilka tabel OpenType musi pojawić się wiele razy, raz dla każdej czcionki dodanej w TTC. Podczas gdy inne tabele mogą być współużytkowane przez wiele czcionek w pliku TTC.

### Nagłówek TTC
Do tej pory dostępne są dwie wersje tabeli nagłówków TTC:
- Wersja 1.0 jest używana dla plików TTC bez podpisów cyfrowych.
- Wersja 2.0 może być używana do plików TTC z podpisami cyfrowymi lub bez.
Oto tabele nagłówków TTC obu wersji:

**Nagłówek TTC wersja 1.0:**

|Typ|Nazwa|Opis|
---|---|---|
|TAG|ttcTag|Ciąg identyfikatora kolekcji czcionek: 'ttcf' (używany dla czcionek z konturami CFF lub CFF2 oraz konturami TrueType)|
|uint16|majorVersion|Główna wersja nagłówka TTC, = 1.|
|uint16|minorVersion|Mniejsza wersja nagłówka TTC, = 0.|
|uint32|numFonts|Liczba czcionek w TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Tablica przesunięć do TableDirectory dla każdej czcionki od początku pliku|

**Nagłówek TTC wersja 2.0:**

|Typ|Nazwa|Opis|
---|---|---|
|TAG|ttcTag |Ciąg identyfikatora kolekcji czcionek: 'ttcf'|
|uint16| majorVersion |Główna wersja nagłówka TTC, = 2.|
|uint16| minorVersion |Mniejsza wersja nagłówka TTC, = 0.|
|uint32| numFonts |Liczba czcionek w TTC|
|Odsunięcie32| tableDirectoryOffsets[numFonts] |Tablica przesunięć do TableDirectory dla każdej czcionki od początku pliku|
|uint32| dsigTag |Znacznik wskazujący, że tabela DSIG istnieje, 0x44534947 („DSIG”) (pusty, jeśli brak podpisu)|
|uint32| dsigLength |Długość (w bajtach) tabeli DSIG (null jeśli brak podpisu)|
|uint32| dsigOffset |Przesunięcie (w bajtach) tabeli DSIG od początku pliku TTC (puste, jeśli brak podpisu)|

## Bibliografia
* [Plik czcionek OpenType](https://docs.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

