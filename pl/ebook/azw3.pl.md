{
  "date" : "2019-12-12",
  "keywords" :["KF8", "rozszerzenie", "plik", "format", "eBook", "Format pliku Kindle", "Struktura pliku AZW3" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się o formacie pliku AZW3 i interfejsach API, które mogą tworzyć i otwierać pliki AZW3.",
  "title" :"Co to jest plik AZW3?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## Czym jest plik AZW3?

AZW3, znany również jako Kindle Format 8 (**KF8**), to zmodyfikowana wersja cyfrowego formatu plików e-booków [AZW](/pl/ebook/azw/) opracowana dla urządzeń Amazon Kindle. Format jest ulepszeniem starszych plików AZW i jest używany na urządzeniach Kindle Fire tylko z kompatybilnością wsteczną dla formatu pliku przodka, tj. [MOBI](/pl/ebook/mobi/) i AZW. Amazon wprowadził format KFX (wersja KF 10) po KF8, który jest używany w najnowszych urządzeniach Kindle. Pliki AZW3 mają aplikację typu media internetowe / vnd.amazon.mobi8-ebook. Pliki AZW3 można konwertować na wiele innych formatów plików, takich jak [PDF](/pl/pdf/), [EPUB](/pl/ebook/epub/), [AZW](/pl/ebook/azw/), [DOCX](/pl/ edytor tekstu/docx/) i [RTF](/pl/procesor tekstu/rtf/).

## Format pliku AZ3/KF8 ##

Pliki KF8 mają charakter binarny i zachowują strukturę formatu pliku MOBI jako plik PDB. Jak wspomniano wcześniej, plik KF8 może składać się zarówno z MOBI, jak i nowszej wersji KF8 EPUB później. Wewnętrzne szczegóły formatu zostały zdekodowane przez [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), który jest skryptem Pythona, który analizuje ostateczną skompilowaną bazę danych i wyodrębnia z niej pliki źródłowe MOBI lub AZW. Pliki AZW3 (KF8) są przeznaczone dla wersji EPUB3 z kompatybilnością wsteczną również dla EPUB. KF8 kompiluje pliki EPUB i generuje strukturę binarną w oparciu o format pliku PDB.

## Bibliografia ##

* [KF8 – z Wikipedii](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Rozpakuj Kindle](https://github.com/kevinhendricks/KindleUnpack)

