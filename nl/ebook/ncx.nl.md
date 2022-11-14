{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "EPUB Navigation Control XML-bestand", "extensie", "format", "E-Book", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over EPUB Navigation Control XML File (NCX)-bestandsindeling en API's die NCX-bestanden kunnen maken en openen.",
  "title" :"NCX - EPUB Navigatiebesturing XML-bestand",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Wat is een NCX-bestand? ##

Het NCX-bestand afgekort als een Navigation Control-bestand voor XML, gewoonlijk toc.ncx genoemd. Dit bestand bestaat uit de hiërarchische inhoudsopgave voor een EPUB-bestand. De specificatie voor NCX is ontwikkeld voor Digital Talking Book (DTB) en dit bestandsformaat wordt onderhouden door het **DAISY Consortium** en maakt geen deel uit van de EPUB-specificatie. Het NCX-bestand bevat een mime-type **application/x-dtbncx+xml** erin.

## NCX-specificatie ##

Het NCX-bestand bevat verschillende soorten XML-tags. De metatags zoals `meta name="dtb:uid"` worden gebruikt om de ID te vermelden. Het `meta name="dtb: depth"` element is gelijk aan de diepte van het `navMap` tag-element. De `navPoint`-elementen kunnen worden genest om een hiërarchische inhoudsopgave te maken. De inhoud van `navLabel` is de tekst die verschijnt in de inhoudsopgave die wordt gegenereerd door leessystemen die de .ncx gebruiken. De inhoud van het `navPoint`-element verwijst naar een inhoudsdocument dat in het manifest wordt vermeld en kan ook een element-ID bevatten

Een beschrijving van bepaalde uitzonderingen op de NCX-specificatie zoals gebruikt in EPUB. Hier kunt u het voorbeeld van een NCX-bestand bekijken:

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

## Referenties ##

* [EPUB van Wikipedia](https://en.wikipedia.org/wiki/EPUB)
* [Welke bestanden moeten worden opgenomen in de toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

