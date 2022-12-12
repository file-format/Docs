{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "EPUB Navigation Control XML File", "extension", "format", "E-Book", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru XML (NCX) souboru EPUB Navigation Control a rozhraní API, která mohou vytvářet a otevírat soubory NCX.",
  "title" :"NCX - soubor XML ovládání navigace EPUB",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Co je soubor NCX? ##

Soubor NCX zkráceně jako soubor ovládání navigace pro XML, obvykle pojmenovaný toc.ncx. Tento soubor se skládá z hierarchického obsahu pro soubor EPUB. Specifikace pro NCX byla vyvinuta pro Digital Talking Book (DTB) a tento formát souboru spravuje **DAISY Consortium** a není součástí specifikace EPUB. Soubor NCX obsahuje typ mime **application/x-dtbncx+xml**.

## Specifikace NCX ##

Soubor NCX obsahuje různé druhy značek XML. K uvedení ID se používají metaznačky jako `meta name="dtb:uid"`. Prvek `meta name="dtb:depth"` je nastaven na stejnou hloubku jako hloubka prvku tagu `navMap`. Prvky `navPoint` lze vnořit a vytvořit tak hierarchický obsah. Obsah `navLabel` je text, který se objeví v obsahu generovaném čtecími systémy, které používají .ncx. Obsah prvku `navPoint` ukazuje na dokument obsahu uvedený v manifestu a může také obsahovat identifikátor prvku

Popis určitých výjimek ze specifikace NCX používané v EPUB. Zde si můžete prohlédnout příklad souboru NCX:

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

## Reference ##

* [EPUB z Wikipedie](https://en.wikipedia.org/wiki/EPUB)
* [Jaké soubory zahrnout do toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

