{
  "date" : "2021-08-17",
  "keywords" :["plik udf", "format pliku udf", "co to jest plik udf", "plik", "przykład udf", "rozszerzenie pliku udf", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Poznaj format plików UDF i interfejsy API, które mogą tworzyć i otwierać pliki UDF.",
  "title" :"UDF - plik formatu dysku uniwersalnego",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## Czym jest plik UDF?
Plik z rozszerzeniem .udf to format obrazu dysku, zwykle używany do zapisywania plików na nośnikach optycznych; może być używany do nagrywania płyt DVD, CD i innych nośników optycznych; przechowuje kolekcję plików przy użyciu struktury katalogów określonej w standardzie UDF; umożliwia usuwanie i modyfikowanie plików na dysku docelowym nawet po ich zapisaniu. Stowarzyszenie Optical Storage Technology Association ustanowiło system plików UDF jako standard w celu utworzenia wspólnego systemu plików dla wszystkich nośników optycznych, takich jak nośniki optyczne wielokrotnego zapisu i nośniki tylko do odczytu.

## Format pliku UDF
Format pliku UDF to otwarty, niezależny od dostawcy system plików do przechowywania danych komputerowych dla szerokiej gamy nośników. Był powszechnie używany w przypadku płyt DVD i nowszych formatów dysków optycznych. Zwykle oprogramowanie opanowuje system plików UDF w procesie wsadowym i zapisuje go na nośniku optycznym w jednym przebiegu. Jednak gdy zapisuje pakiety na nośnikach wielokrotnego zapisu, UDF umożliwia tworzenie, usuwanie i zmienianie plików na dysku, podobnie jak system plików ogólnego przeznaczenia na nośnikach wymiennych, takich jak dyski flash lub dyskietki.
### Specyfikacje UDF
Standard UDF definiuje następujące trzy warianty systemu plików:

- **Zwykła kompilacja**: jest to oryginalny format obsługiwany we wszystkich wersjach UDF. Został wprowadzony w pierwszej wersji standardu, format ten może być używany na dowolnym typie dysku, który umożliwia swobodny dostęp do odczytu lub zapisu, takich jak DVD+RW, dyski twarde i nośniki DVD-RAM.
- **Kompilacja VAT**: używana specjalnie do zapisywania na nośnikach jednokrotnego zapisu. VAT to dodatkowa struktura na dysku, która umożliwia zapis pakietowy; to znaczy ponowne mapowanie bloków fizycznych, gdy pliki lub inne dane na dysku są modyfikowane lub usuwane. W przypadku nośników jednokrotnego zapisu cały dysk jest zwirtualizowany, dzięki czemu charakter jednokrotnego zapisu jest przejrzysty dla użytkownika; dysk można traktować tak samo, jak dysk wielokrotnego zapisu.
- **Kompilacja Spared (RW)**: używana specjalnie do zapisywania na nośnikach wielokrotnego zapisu. Dodaje dodatkową tabelę zapasową, aby zarządzać błędami, które ostatecznie wystąpią na częściach dysku, które były wielokrotnie przepisywane. Ta tabela zapisuje ślady zużytych sektorów i mapuje je na działające. Zarządzanie defektami UDF nie ma zastosowania do systemów, które już zaimplementowały inną formę zarządzania defektami, taką jak Mount Rainier (MRW) dla dysków optycznych lub kontroler dysku dla dysku twardego.
 




## Bibliografia


* [Format Windows Imaging – Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


