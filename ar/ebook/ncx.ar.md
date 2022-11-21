{
  "date" : "2021-03-23",
  "keywords" :["NCX", "EPUB Navigation Control XML File", "extension", "format", "E-Book", "TOC", "DAISY Consortium"] ,
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف EPUB Navigation Control XML File (NCX) وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات NCX وفتحها." ,
  "title" :"NCX - EPUB Navigation Control XML File" ,
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
} ,
  "lastmod" : "2021-03-22"
}

## ما هو ملف NCX؟ ##

يتم اختصار ملف NCX كملف Navigation Control لـ XML ، وعادةً ما يُسمى toc.ncx. يتكون هذا الملف من جدول محتويات هرمي لملف EPUB. تم تطوير مواصفات NCX لـ Digital Talking Book (DTB) ويتم الحفاظ على تنسيق الملف هذا بواسطة ** DAISY Consortium ** ولا يعد جزءًا من مواصفات EPUB. يتضمن ملف NCX نوع mime من ** application / x-dtbncx + xml ** فيه.

## مواصفات NCX ##

يحتوي ملف NCX على أنواع مختلفة من علامات XML. يتم استخدام العلامات الوصفية مثل `meta name =" dtb: uid "` لذكر المعرف. تم تعيين عنصر `meta name =" dtb: deep "` مساويًا لعمق عنصر العلامة `navMap`. يمكن أن تتداخل عناصر `navPoint` لإنشاء جدول محتويات متدرج. محتوى "navLabel" هو النص الذي يظهر في جدول المحتويات الذي تم إنشاؤه بواسطة أنظمة القراءة التي تستخدم .ncx. يشير محتوى عنصر "navPoint" إلى مستند محتوى مدرج في البيان ويمكن أن يتضمن أيضًا معرف عنصر

وصف لبعض الاستثناءات لمواصفات NCX كما هو مستخدم في EPUB. هنا يمكنك عرض مثال لملف NCX:

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

## مراجع ##

* [EPUB From Wikipedia] (https://en.wikipedia.org/wiki/EPUB)
* [ما هي الملفات المراد تضمينها في toc.ncx] (https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

