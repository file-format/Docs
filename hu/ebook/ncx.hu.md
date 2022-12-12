{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "EPUB Navigation Control XML File", "extension", "format", "E-Book", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az EPUB Navigation Control XML File(NCX) fájlformátumról és az NCX-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"NCX - EPUB Navigation Control XML fájl",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Mi az NCX fájl? ##

Az NCX fájl rövidítése az XML navigációs vezérlőfájlja, általában toc.ncx néven. Ez a fájl egy EPUB-fájl hierarchikus tartalomjegyzékét tartalmazza. Az NCX specifikációját a Digital Talking Book (DTB) számára fejlesztették ki, és ezt a fájlformátumot a **DAISY Consortium** tartja karban, és nem része az EPUB specifikációnak. Az NCX fájl egy **application/x-dtbncx+xml** MIME típusú fájlt tartalmaz.

## NCX specifikáció ##

Az NCX fájl különféle XML-címkéket tartalmaz. A metacímkék, például a `meta name="dtb:uid"` az azonosító említésére szolgálnak. A `meta name="dtb:depth"` elem a `navMap` címkeelem mélységével egyenlő. A "navPoint" elemek egymásba ágyazhatók hierarchikus tartalomjegyzék létrehozásához. A "navLabel" tartalma az a szöveg, amely az .ncx-et használó olvasórendszerek által generált tartalomjegyzékben jelenik meg. A "navPoint" elem tartalma a jegyzékben felsorolt tartalmi dokumentumra mutat, és tartalmazhat egy elemazonosítót is

Az EPUB-ban használt NCX-specifikáció alóli bizonyos kivételek leírása. Itt megtekintheti egy NCX fájl példáját:

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

## Referenciák ##

* [EPUB a Wikipédiából](https://en.wikipedia.org/wiki/EPUB)
* [Milyen fájlok szerepeljenek a toc.ncx fájlban](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

