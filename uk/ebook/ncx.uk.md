{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "XML-файл керування навігацією EPUB", "розширення", "формат", "Електронна книга", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу EPUB Navigation Control XML File (NCX) та API, які можуть створювати та відкривати файли NCX.",
  "title" :"NCX - XML-файл керування навігацією EPUB",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Що таке файл NCX? ##

Файл NCX скорочено називається файлом керування навігацією для XML, зазвичай називається toc.ncx. Цей файл складається з ієрархічного змісту файлу EPUB. Специфікація для NCX була розроблена для Digital Talking Book (DTB), і цей формат файлу підтримується **DAISY Consortium** і не є частиною специфікації EPUB. Файл NCX містить тип mime **application/x-dtbncx+xml**.

## Специфікація NCX ##

Файл NCX містить різноманітні теги XML. Метатеги, такі як `meta name="dtb:uid"`, використовуються для згадування ідентифікатора. Елемент `meta name="dtb:depth"` встановлюється рівним глибині елемента тегу `navMap`. Елементи `navPoint` можна вкладати, щоб створити ієрархічний зміст. Вміст `navLabel` — це текст, який відображається у змісті, створеному системами читання, які використовують .ncx. Вміст елемента `navPoint` вказує на документ із вмістом, указаний у маніфесті, а також може містити ідентифікатор елемента

Опис певних винятків із специфікації NCX, яка використовується в EPUB. Тут ви можете переглянути приклад файлу NCX:

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

## Посилання ##

* [EPUB з Вікіпедії](https://en.wikipedia.org/wiki/EPUB)
* [Які файли включити в toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

