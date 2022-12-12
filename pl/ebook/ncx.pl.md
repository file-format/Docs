{
  "date" : "2021-03-23",
  "keywords" :["NCX", "EPUB Navigation Control XML File", "extension", "format", "E-Book", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się więcej o formacie plików EPUB Navigation Control XML File (NCX) i interfejsach API, które mogą tworzyć i otwierać pliki NCX.",
  "title" :"NCX - plik kontrolny nawigacji EPUB XML",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Czym jest plik NCX? ##

Plik NCX w skrócie jako plik sterowania nawigacją dla XML, zwykle nazywany toc.ncx. Ten plik składa się z hierarchicznego spisu treści dla pliku EPUB. Specyfikacja NCX została opracowana dla Digital Talking Book (DTB), a ten format pliku jest obsługiwany przez **konsorcjum DAISY** i nie jest częścią specyfikacji EPUB. Plik NCX zawiera typ MIME **application/x-dtbncx+xml**.

## Specyfikacja NCX ##

Plik NCX zawiera różne rodzaje znaczników XML. Metatagi, takie jak `meta name="dtb:uid"` są używane do podania identyfikatora. Element `meta name="dtb:depth"` jest ustawiony na głębokość elementu znacznika `navMap`. Elementy `navPoint` można zagnieżdżać w celu utworzenia hierarchicznego spisu treści. Zawartość `navLabel` to tekst, który pojawia się w spisie treści generowanym przez systemy odczytujące używające .ncx. Zawartość elementu „navPoint” wskazuje na dokument treści wymieniony w manifeście i może również zawierać identyfikator elementu

Opis niektórych wyjątków od specyfikacji NCX stosowanej w EPUB. Tutaj możesz zobaczyć przykład pliku NCX:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ncx PUBLIC "-//NISO//DTD ncx 2005-1//EN"
"http://www.daisy.org/z3986/2005/ncx-2005-1.dtd">

<ncx version="2005-1" xml:lang="en" xmlns="http://www.daisy.org/z3986/2005/ncx/">

  <head>
<!-- The following four metadata items are required for all NCX documents,
including those that conform to the relaxed constraints of OPS 2.0 -->

    <meta name="dtb:uid" content="123456789X"/> <!-- same as in .opf -->
    <meta name="dtb:depth" content="1"/> <!-- 1 or higher -->
    <meta name="dtb:totalPageCount" content="0"/> <!-- must be 0 -->
    <meta name="dtb:maxPageNumber" content="0"/> <!-- must be 0 -->
  </head>

  <docTitle>
    <text>Pride and Prejudice</text>
  </docTitle>

  <docAuthor>
    <text>Austen, Jane</text>
  </docAuthor>

  <navMap>
    <navPoint class="chapter" id="chapter1" playOrder="1">
      <navLabel><text>Chapter 1</text></navLabel>
      <content src="chapter1.xhtml"/>
    </navPoint>
  </navMap>

</ncx>
```

## Bibliografia ##

* [EPUB z Wikipedii](https://en.wikipedia.org/wiki/EPUB)
* [Jakie pliki dołączyć do toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

