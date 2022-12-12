{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "EPUB XML файл за контрол на навигацията", "разширение", "формат", "Електронна книга", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за EPUB файловия формат за XML файл за контрол на навигацията (NCX) и API, които могат да създават и отварят NCX файлове.",
  "title" :"NCX – EPUB XML файл за контрол на навигацията",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Какво е NCX файл? ##

Файлът NCX, съкратено като файл за контрол на навигацията за XML, обикновено наречен toc.ncx. Този файл се състои от йерархичното съдържание на EPUB файл. Спецификацията за NCX е разработена за Digital Talking Book (DTB) и този файлов формат се поддържа от **DAISY Consortium** и не е част от EPUB спецификацията. NCX файлът включва mime тип от **application/x-dtbncx+xml** в него.

## NCX Спецификация ##

NCX файлът съдържа различни видове XML тагове. Мета таговете като `meta name="dtb:uid"` се използват за споменаване на ID. Елементът `meta name="dtb:depth"` е зададен равен на дълбочината на елемента на етикета `navMap`. Елементите `navPoint` могат да бъдат вложени, за да се създаде йерархична таблица със съдържание. Съдържанието на `navLabel` е текстът, който се появява в таблицата със съдържание, генерирана от системи за четене, които използват .ncx. Съдържанието на елемента „navPoint“ сочи към документ със съдържание, посочен в манифеста, и може също да включва идентификатор на елемент

Описание на определени изключения от спецификацията NCX, както се използва в EPUB. Тук можете да видите примера на NCX файл:

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

## Препратки ##

* [EPUB от Wikipedia](https://en.wikipedia.org/wiki/EPUB)
* [Какви файлове да включите в toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

