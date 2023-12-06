{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik CPIO - Unixowy format pliku archiwum CPIO",
  "description":"Dowiedz się, co to jest plik CPIO i interfejsy API, które umożliwiają tworzenie i otwieranie plików CPIO.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## .CPIO opcja № 1

Plik CPIO to plik archiwum utworzony w formacie Unix Copy In Copy Out (CPIO). Jest podobny do formatu pliku TAR, z tą różnicą, że jest nieskompresowany. Pliki CPIO mogą przechowywać pliki urządzeń, dowiązania symboliczne i rozszerzone atrybuty plików.

## Format pliku CPIO

Archiwum CPIO jest tworzone jako plik binarny, który nie jest czytelny dla człowieka. Przechowuje kolekcję plików i katalogów. Zawartość archiwum CPIO jest identyfikowana za pomocą metadanych, takich jak nazwy plików, uprawnienia, własność i znaczniki czasu. Te metadane są również przechowywane w pliku archiwum, do którego system ma dostęp boczny.

## Format Archiwum CPIO

Plik CPIO składa się z jednego lub większej liczby połączonych plików członkowskich. Każdy plik w archiwum składa się z nagłówka, po którym opcjonalnie następuje zawartość pliku wymieniona w nagłówku. Archiwum zawiera na końcu kolejny nagłówek opisany pustym plikiem o nazwie TRAILER!!.

### Rodzaje archiwów CPIO

Istnieją dwa typy archiwów CPIO. Różnią się one jedynie stylem nagłówka.

* Archiwa ASCII — te archiwa CPIO mają drukowalny nagłówek, który staje się częścią archiwum CPIO, jeśli samo archiwum składa się z plików ASCII
* Archiwa binarne — te archiwa CPIO mają nagłówki binarne.

## Praca z Archiwum CPIO

### Jak utworzyć archiwa CPIO?

Możesz utworzyć CPIO w systemach uniksowych za pomocą polecenia **cpio**. Poniższe polecenie znajdzie wszystkie pliki i katalogi w bieżącym katalogu i jego podkatalogach. Dane wyjściowe są następnie przesyłane do polecenia cpio, które wygeneruje nowe archiwum CPIO o nazwie Archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Jak wyodrębnić pliki z archiwów CPIO?

Poniższe polecenie wyodrębnia pliki z istniejącego archiwum.

```
cpio -id < archive_cpio.cpio
```
Odczyta plik Archive.cpio ze standardowego wejścia i wyodrębni pliki do bieżącego katalogu.


## Bibliografia

* [CPIO – według Wikipedii](https://en.wikipedia.org/wiki/Cpio)
* [Format pliku CPIO](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

