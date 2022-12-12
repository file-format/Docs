{
  "date" : "2019-10-11",
  "keywords" :[ "plik wmf", "format pliku wmf", "co to jest plik wmf", "plik", "przykład wmf", "rozszerzenie pliku wmf", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF — format metapliku Microsoft Windows",
  "description":"Poznaj format plików WMF i interfejsy API, które mogą tworzyć i otwierać pliki WMF.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik WMP?

Pliki z rozszerzeniem WMF reprezentują Microsoft Windows Metafile (WMF) do przechowywania danych obrazów wektorowych i bitmapowych. Aby być dokładniejszym, WMF należy do kategorii formatów plików wektorowych formatów plików graficznych, która jest niezależna od urządzenia. Windows Graphical Device Interface (GDI) używa funkcji zapisanych w pliku WMF do wyświetlania obrazu na ekranie. Bardziej ulepszona wersja WMF, znana jako Enhanced Meta Files (EMF), została opublikowana później, dzięki czemu format jest bogatszy w funkcje. Praktycznie WMF są podobne do SVG.

## Specyfikacje formatu plików WMF ##

Plik WMF odnosił się do 16-bitowego formatu pliku w momencie jego uruchomienia w systemie Windows 3.0. Format pliku składa się z serii rekordów o zmiennej długości, które zawierają polecenia rysowania grafiki, definicje obiektów i właściwości. Ponieważ pliki WMF są oparte na poleceniach renderowanych do GDI w celu narysowania obrazu, jest to również znane jako cyfrowe nagranie obrazu, które można odtworzyć w celu odtworzenia tego obrazu. Pełne specyfikacje formatu plików WMF są dostępne online i należy się z nimi zapoznać przy opracowywaniu aplikacji do pracy z plikami WMF. Plik WMF jest zorganizowany w:

* Rekord nagłówka WMF
* Rekord (y) WMF
* Rekord końca pliku WMF

### Rekord nagłówka WMF ###

**Rekord META_HEADER** zawiera informacje określające cechy metapliku, w tym:

* Typ metapliku
* Wersja metapliku
* Rozmiar metapliku
* Liczba obiektów zdefiniowanych w metapliku
* Rozmiar największego pojedynczego rekordu w metapliku

### WMF Umieszczalny rekord nagłówka ###

**Rekord META_PLACEABLE** zawiera rozszerzone informacje dotyczące obrazu, w tym:

* Prostokąt ograniczający
* Rozmiar jednostki logicznej do skalowania
* Suma kontrolna do weryfikacji

### Rekord WMF ###

Rekordy WMF mają ogólny format, który jest określony w dokumencie specyfikacji. Każdy rekord WMF zawiera następujące informacje:

* Rozmiar rekordu
* Funkcja nagrywania
* Parametry, jeśli istnieją, dla funkcji nagrywania

## Bibliografia ##

* [[MS-WMF]: Windows Metafile Format](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Metaplik systemu Windows – Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

