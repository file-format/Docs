{
  "date" : "2019-12-12",
  "keywords" :["CBC", "rozszerzenie", "plik", "format", "Komiksy", "Format pliku komiksów", "eBook"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku CBC i interfejsy API, które mogą tworzyć i otwierać pliki CBC.",
  "title" :"CBC — format pliku kolekcji komiksów",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## Czym jest plik CBC?

Plik z rozszerzeniem .cbc to skompresowana kolekcja plików komiksów dla eBooków i zawiera pliki [CBZ](/pl/ebook/cbz/) i [CBR](/pl/ebook/cbr/). Jest używany przez [Calibre](https://calibre-ebook.com/), aplikację do konwersji e-booków, która jest wieloplatformowym menedżerem e-booków typu open source i pozwala zarządzać e-bookami i konwertować je do różnych formatów . Plik CBC zawiera plik .txt, comics.txt, który zawiera listę innych plików wchodzących w skład archiwum. W Internecie dostępnych jest kilka aplikacji, które mogą konwertować pliki CBC do formatów [AZW3](/pl/ebook/azw3), [EPUB](/pl/ebook/epub/), [FB2](/pl/ebook/fb2/), [MOBI](/pl/ebook/ mobi/), [TXT](/pl/word-processing/txt/), [PDF](/pl/pdf/) i inne popularne formaty plików.

## Format pliku CBC

Pliki CBC to skompresowane archiwa zawierające CBZ, CBR i plik tekstowy do wyświetlania zawartości. Plik tekstowy comics.txt jest zakodowany w UTF8 i zawiera listę plików CBC, których czytelnicy mogą używać do organizowania swoich kolekcji. Plik CBC ma zwykle kilka atrybutów, które umożliwiają organizację tej kolekcji, takich jak Komiks, Kategoria, Wydawca, Seria, Wydanie i Artysta.

Zawartość przykładowego pliku CBC jest wymieniona w następujący sposób:

* comics.txt - Plik tekstowy zawierający listę plików CBR i CBZ
* 1.cbz
* 2.cbz
* 3.cbz
* plik(i) CBZ

gdzie plik comics.txt zawiera następującą listę zawartości:

* 1.cbz: Rozdział pierwszy
* 2.cbz: Rozdział drugi
* 3.cbz: Rozdział trzeci

Czytelnicy przetwarzają plik comics.txt i na podstawie podanych danych generują spis treści.

## Bibliografia

* [Kaliber](https://calibre-ebook.com/)

