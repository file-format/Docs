{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "EPUB Navigation Control XML-fil", "tillägg", "format", "E-Book", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om EPUB Navigation Control XML File(NCX)-filformat och API:er som kan skapa och öppna NCX-filer.",
  "title" :"NCX - EPUB Navigation Control XML-fil",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Vad är en NCX fil? ##

NCX-filen förkortas som en Navigation Control-fil för XML, vanligtvis kallad toc.ncx. Den här filen består av den hierarkiska innehållsförteckningen för en EPUB-fil. Specifikationen för NCX utvecklades för Digital Talking Book (DTB) och detta filformat underhålls av **DAISY Consortium** och är inte en del av EPUB-specifikationen. NCX-filen innehåller en mime-typ av **applikation/x-dtbncx+xml** i den.

## NCX-specifikation ##

NCX-filen innehåller olika typer av XML-taggar. Metataggar som `meta name="dtb:uid"` används för att nämna ID. Elementet `meta name="dtb:depth"` sätts lika med djupet för taggelementet `navMap`. `navPoint`-elementen kan kapslas för att skapa en hierarkisk innehållsförteckning. Innehållet i `navLabel` är texten som visas i innehållsförteckningen som genereras av lässystem som använder .ncx. Innehållet i elementet "navPoint" pekar på ett innehållsdokument listat i manifestet och kan även inkludera en elementidentifierare

En beskrivning av vissa undantag från NCX-specifikationen som används i EPUB. Här kan du se exemplet på en NCX-fil:

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

## Referenser ##

* [EPUB från Wikipedia](https://en.wikipedia.org/wiki/EPUB)
* [Vilka filer som ska inkluderas i toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

