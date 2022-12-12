{
  "date" : "2019-10-11",
  "keywords" :["plik tar", "format pliku tar", "co to jest plik tar", "plik", "przykład tar", "rozszerzenie pliku tar", "rozszerzenie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Unix Archive File Format",
  "description":"Dowiedz się, czym jest plik Tar i interfejsy API, które mogą tworzyć i otwierać pliki TAR.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik TAR?

Pliki z rozszerzeniem .tar to archiwa utworzone za pomocą narzędzia opartego na systemie Unix do gromadzenia jednego lub więcej plików. Wiele plików jest przechowywanych w nieskompresowanym formacie z obsługą dodawania plików i folderów do archiwum. Narzędzie TAR w systemie Unix jest oparte na poleceniach, ale utworzone w ten sposób pliki są obsługiwane przez większość systemów archiwizacji plików w prawie wszystkich systemach operacyjnych. Po raz pierwszy została stworzona w 1979 roku przez AT&T Bell Laboratories, a kolejne wersje były publikowane z upływem czasu.

## Format pliku TAR

TAR to otwarty format pliku z pełną specyfikacją dostępną dla programistów. Jego struktura plików została znormalizowana w POSIX.1-1988, a później w POSIX.1-2001. Zestawy danych utworzone przez tar zachowują informacje o parametrach systemu plików, takich jak:

* Nazwa
* Znaczniki czasu
* Własność
* Uprawnienia dostępu do plików
* Organizacja katalogów

Plik Tar nie ma żadnej magicznej liczby. Zawiera serię bloków, z których każdy ma rozmiar BLOCKSIZE bajtów.

Każdy zarchiwizowany plik jest reprezentowany przez blok nagłówka, który opisuje plik, po którym następuje zero lub więcej bloków, które określają zawartość pliku. Na końcu pliku archiwum znajdują się dwa 512-bajtowe bloki wypełnione binarnymi zerami jako znacznikiem końca pliku. Rozsądny system powinien zapisywać taki znacznik końca pliku na końcu archiwum, ale nie może zakładać, że taki blok istnieje podczas odczytu archiwum. W szczególności GNU tar zawsze wyświetla ostrzeżenie, jeśli go nie napotka.

Bloki mogą być blokowane dla fizycznych operacji we/wy. Każdy rekord złożony z n bloków (gdzie n jest ustawiany przez opcję tar parametru blocking-factor = 512-size) jest zapisywany za pomocą pojedynczej operacji „write()”. Na taśmach magnetycznych wynikiem takiego zapisu jest pojedynczy zapis. Podczas zapisywania archiwum ostatni zapis bloków powinien być zapisywany w pełnym rozmiarze, z blokami po bloku zerowym zawierającym same zera. Przy czytaniu archiwum rozsądny system powinien poprawnie obsłużyć archiwum, którego ostatni rekord jest krótszy niż pozostałe lub które zawiera rekordy śmieci po bloku zerowym.

### Nagłówek Tar

Podobnie jak inne nagłówki plików, rekord nagłówka pliku tar zawiera metadane dotyczące pliku i jest przedstawiony w poniższej tabeli.


|Przesunięcie pola|Rozmiar pola (bajty)|Pole
---|---|---|
|0|100|Nazwa pliku
|100|8|Tryb pliku
|108|8|Numeryczny identyfikator użytkownika właściciela
|116|8|Numeryczny identyfikator użytkownika grupy
|124|12|Rozmiar pliku w bajtach (podstawa ósemkowa)
|136|12|Czas ostatniej modyfikacji w numerycznym formacie czasu Unix (ósemkowo)
|148|8|Suma kontrolna dla rekordu nagłówka
|156|1|Wskaźnik łącza (typ pliku)
|157|100|Nazwa połączonego pliku

Nieużywane pola są wypełniane bajtami NUL. Nagłówek składa się z 257 bajtów, które są uzupełniane bajtami NUL, aby wypełnić rekord o długości 512 bajtów.

## Bibliografia ##

* [TAR – z Wikipedii](https://en.wikipedia.org/wiki/Tar_(komputery))
* [Podstawowy format TAR](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

