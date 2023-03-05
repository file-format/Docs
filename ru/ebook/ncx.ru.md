{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "XML-файл управления навигацией EPUB", "расширение", "формат", "Электронная книга", "TOC", "Консорциум DAISY"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файла EPUB Navigation Control XML File (NCX) и API-интерфейсах, которые могут создавать и открывать файлы NCX.",
  "title" :"NCX — XML-файл управления навигацией EPUB",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## .NCX вариант № ##

Файл NCX, сокращенно называемый файлом управления навигацией для XML, обычно называется toc.ncx. Этот файл состоит из иерархического оглавления файла EPUB. Спецификация NCX была разработана для Digital Talking Book (DTB), и этот формат файла поддерживается **DAISY Consortium** и не является частью спецификации EPUB. Файл NCX включает в себя MIME-тип **application/x-dtbncx+xml**.

## Спецификация NCX ##

Файл NCX содержит различные типы тегов XML. Метатеги типа `meta name="dtb:uid"` используются для упоминания идентификатора. Элемент `meta name="dtb:depth"` устанавливается равным глубине элемента тега `navMap`. Элементы `navPoint` могут быть вложены друг в друга для создания иерархического оглавления. Содержимое `navLabel` — это текст, который появляется в оглавлении, сгенерированном системами чтения, использующими .ncx. Содержимое элемента `navPoint` указывает на документ содержимого, указанный в манифесте, и может также включать идентификатор элемента.

Описание некоторых исключений из спецификации NCX, используемых в EPUB. Здесь вы можете просмотреть пример файла NCX:

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

## Использованная литература ##

* [EPUB из Википедии](https://en.wikipedia.org/wiki/EPUB)
* [Какие файлы включить в toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

