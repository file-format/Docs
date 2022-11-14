{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "EPUB 탐색 제어 XML 파일", "확장자", "형식", "전자책", "목차", "데이지 컨소시엄"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"NCX 파일을 생성하고 열 수 있는 EPUB Navigation Control XML File(NCX) 파일 형식과 API에 대해 알아보세요.",
  "title" :"NCX - EPUB 탐색 제어 XML 파일",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## .NCX 파일이란? ##

NCX 파일은 일반적으로 toc.ncx라는 XML용 탐색 제어 파일로 축약됩니다. 이 파일은 EPUB 파일의 계층적 목차로 구성됩니다. NCX 사양은 DTB(Digital Talking Book)용으로 개발되었으며 이 파일 형식은 **DAISY Consortium**에서 유지 관리되며 EPUB 사양의 일부가 아닙니다. NCX 파일에는 **application/x-dtbncx+xml**의 MIME 형식이 포함되어 있습니다.

## NCX 사양 ##

NCX 파일에는 다양한 종류의 XML 태그가 포함되어 있습니다. `meta name="dtb:uid"`와 같은 메타 태그는 ID를 언급하는 데 사용됩니다. `meta name="dtb:depth"` 요소는 `navMap` 태그 요소의 깊이와 동일하게 설정됩니다. 'navPoint' 요소를 중첩하여 계층적 목차를 만들 수 있습니다. 'navLabel'의 내용은 .ncx를 사용하는 읽기 시스템에서 생성된 목차에 나타나는 텍스트입니다. 'navPoint' 요소의 콘텐츠는 매니페스트에 나열된 콘텐츠 문서를 가리키며 요소 식별자도 포함할 수 있습니다.

EPUB에서 사용되는 NCX 사양의 특정 예외에 대한 설명입니다. 여기에서 NCX 파일의 예를 볼 수 있습니다.

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

## 참조 ##

* [위키피디아의 EPUB](https://en.wikipedia.org/wiki/EPUB)
* [toc.ncx에 포함할 파일](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

