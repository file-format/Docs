{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "File XML di controllo della navigazione EPUB", "estensione", "formato", "E-Book", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Ulteriori informazioni sul formato file EPUB Navigation Control XML File (NCX) e sulle API che possono creare e aprire file NCX.",
  "title" :"NCX - File XML di controllo della navigazione EPUB",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Che cos'è un file NCX? ##

Il file NCX abbreviato in un file di controllo della navigazione per XML, solitamente denominato toc.ncx. Questo file è costituito dal sommario gerarchico di un file EPUB. La specifica per NCX è stata sviluppata per Digital Talking Book (DTB) e questo formato di file è gestito dal **DAISY Consortium** e non fa parte della specifica EPUB. Il file NCX include un tipo mime di **application/x-dtbncx+xml** al suo interno.

## Specifica NCX ##

Il file NCX contiene vari tipi di tag XML. I meta tag come `meta name="dtb:uid"` sono usati per menzionare l'ID. L'elemento `meta name="dtb:depth"` è impostato uguale alla profondità dell'elemento tag `navMap`. Gli elementi `navPoint` possono essere annidati per creare un sommario gerarchico. Il contenuto di `navLabel` è il testo che compare nel sommario generato dai sistemi di lettura che utilizzano il .ncx. Il contenuto dell'elemento `navPoint` punta a un documento di contenuto elencato nel manifest e può anche includere un identificatore di elemento

Una descrizione di alcune eccezioni alla specifica NCX utilizzata in EPUB. Qui puoi vedere l'esempio di un file NCX:

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

## Riferimenti ##

* [EPUB da Wikipedia](https://en.wikipedia.org/wiki/EPUB)
* [Quali file includere nel toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

