{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "EPUB Navigation Control XML File", "extension", "format", "E-Book", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das Dateiformat EPUB Navigation Control XML File (NCX) und APIs, die NCX-Dateien erstellen und öffnen können.",
  "title" :"NCX - XML-Datei zur EPUB-Navigationssteuerung",
  "linktitle" :"NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Was ist eine NCX-Datei? ##

Die NCX-Datei, abgekürzt als Navigationssteuerungsdatei für XML, normalerweise mit dem Namen toc.ncx. Diese Datei besteht aus dem hierarchischen Inhaltsverzeichnis einer EPUB-Datei. Die Spezifikation für NCX wurde für Digital Talking Book (DTB) entwickelt und dieses Dateiformat wird vom **DAISY Consortium** gepflegt und ist nicht Teil der EPUB-Spezifikation. Die NCX-Datei enthält einen Mime-Typ von **application/x-dtbncx+xml** darin.

## NCX-Spezifikation ##

Die NCX-Datei enthält verschiedene Arten von XML-Tags. Die Meta-Tags wie `meta name="dtb:uid"` werden verwendet, um die ID zu erwähnen. Das `meta name="dtb:depth"`-Element wird gleich der Tiefe des `navMap`-Tag-Elements gesetzt. Die `navPoint`-Elemente können verschachtelt werden, um ein hierarchisches Inhaltsverzeichnis zu erstellen. Der Inhalt von „navLabel“ ist der Text, der im Inhaltsverzeichnis erscheint, das von Lesesystemen generiert wird, die das .ncx verwenden. Der Inhalt des Elements „navPoint“ verweist auf ein im Manifest aufgeführtes Inhaltsdokument und kann auch eine Elementkennung enthalten

Eine Beschreibung bestimmter Ausnahmen von der NCX-Spezifikation, wie sie in EPUB verwendet wird. Hier sehen Sie das Beispiel einer NCX-Datei:

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

## Verweise ##

* [EPUB aus Wikipedia](https://en.wikipedia.org/wiki/EPUB)
* [Welche Dateien sollen in die toc.ncx aufgenommen werden](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

