{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "Archivo XML de control de navegación EPUB", "extensión", "formato", "Libro electrónico", "TOC", "Consorcio DAISY"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo EPUB Navigation Control XML File (NCX) y las API que pueden crear y abrir archivos NCX",
  "title" :"NCX - Archivo XML de control de navegación EPUB",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## ¿Qué es un archivo NCX? ##

El archivo NCX, abreviado como archivo de control de navegación para XML, generalmente denominado toc.ncx. Este archivo consta de la tabla de contenido jerárquica de un archivo EPUB. La especificación para NCX se desarrolló para Digital Talking Book (DTB) y este formato de archivo lo mantiene **DAISY Consortium** y no forma parte de la especificación EPUB. El archivo NCX incluye un tipo MIME de **aplicación/x-dtbncx+xml**.

## Especificación NCX ##

El archivo NCX contiene varios tipos de etiquetas XML. Las metaetiquetas como `meta name="dtb:uid"` se utilizan para mencionar el ID. El elemento `meta name="dtb: depth"` se establece igual a la profundidad del elemento de etiqueta `navMap`. Los elementos `navPoint` se pueden anidar para crear una tabla de contenido jerárquica. El contenido de `navLabel` es el texto que aparece en la tabla de contenido generada por los sistemas de lectura que usan el .ncx. El contenido del elemento `navPoint` apunta a un documento de contenido que figura en el manifiesto y también puede incluir un identificador de elemento

Una descripción de ciertas excepciones a la especificación NCX como se usa en EPUB. Aquí puede ver el ejemplo de un archivo NCX:

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

## Referencias ##

* [EPUB de Wikipedia](https://en.wikipedia.org/wiki/EPUB)
* [Qué archivos incluir en toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

