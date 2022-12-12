{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "EPUB Navigation Control XML File", "extensie", "format", "E-Book", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier EPUB Navigation Control XML File (NCX) și despre API-urile care pot crea și deschide fișiere NCX.",
  "title" :"NCX - Fișier XML de control al navigării EPUB",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Ce este un fișier NCX? ##

Fișierul NCX abreviat ca fișier de control de navigare pentru XML, numit de obicei toc.ncx. Acest fișier constă din cuprinsul ierarhic pentru un fișier EPUB. Specificația pentru NCX a fost dezvoltată pentru Digital Talking Book (DTB) și acest format de fișier este menținut de **DAISY Consortium** și nu face parte din specificația EPUB. Fișierul NCX include un tip mime de **application/x-dtbncx+xml** în el.

## Specificație NCX ##

Fișierul NCX conține diferite tipuri de etichete XML. Etichetele meta precum `meta name="dtb:uid"` sunt folosite pentru a menționa ID-ul. Elementul `meta name="dtb:depth"` este setat egal cu adâncimea elementului etichetei `navMap`. Elementele `navPoint` pot fi imbricate pentru a crea un cuprins ierarhic. Conținutul `navLabel` este textul care apare în cuprinsul generat de sistemele de citire care utilizează .ncx. Conținutul elementului „navPoint” indică un document de conținut listat în manifest și poate include, de asemenea, un identificator de element

O descriere a anumitor excepții de la specificația NCX așa cum sunt utilizate în EPUB. Aici puteți vizualiza exemplul unui fișier NCX:

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

## Referințe ##

* [EPUB din Wikipedia](https://en.wikipedia.org/wiki/EPUB)
* [Ce fișiere să includă în toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

