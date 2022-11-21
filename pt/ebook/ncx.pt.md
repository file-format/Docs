{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "Arquivo XML de controle de navegação EPUB", "extensão", "formato", "E-Book", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo EPUB Navigation Control XML File(NCX) e APIs que podem criar e abrir arquivos NCX.",
  "title" :"NCX - Arquivo XML de controle de navegação EPUB",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## O que é um arquivo NCX? ##

O arquivo NCX abreviado como um arquivo de controle de navegação para XML, geralmente denominado toc.ncx. Este arquivo consiste no índice hierárquico de um arquivo EPUB. A especificação para NCX foi desenvolvida para Digital Talking Book (DTB) e este formato de arquivo é mantido pelo **DAISY Consortium** e não faz parte da especificação EPUB. O arquivo NCX inclui um tipo mime de **application/x-dtbncx+xml** nele.

## Especificação NCX ##

O arquivo NCX contém vários tipos de tags XML. As meta tags como `meta name="dtb:uid"` são usadas para mencionar o ID. O elemento `meta name="dtb:depth"` é definido como a profundidade do elemento da tag `navMap`. Os elementos `navPoint` podem ser aninhados para criar um índice hierárquico. O conteúdo do `navLabel` é o texto que aparece no índice gerado pelos sistemas de leitura que usam o .ncx. O conteúdo do elemento `navPoint` aponta para um documento de conteúdo listado no manifesto e também pode incluir um identificador de elemento

Uma descrição de certas exceções à especificação NCX conforme usada no EPUB. Aqui você pode ver o exemplo de um arquivo NCX:

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

## Referências ##

* [EPUB da Wikipedia](https://en.wikipedia.org/wiki/EPUB)
* [Quais arquivos incluir no toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

