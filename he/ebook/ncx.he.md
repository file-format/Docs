{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "קובץ XML בקרת ניווט EPUB", "הרחבה", "פורמט", "ספר אלקטרוני", "TOC", "קונסורציום DAISY"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ XML של בקרת ניווט EPUB (NCX) וממשקי API שיכולים ליצור ולפתוח קובצי NCX.",
  "title" :"NCX - קובץ XML בקרת ניווט EPUB",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## מהו קובץ NCX? ##

קובץ ה-NCX מקוצר כקובץ בקרת ניווט עבור XML, בדרך כלל בשם toc.ncx. קובץ זה מורכב מתוכן העניינים ההיררכי עבור קובץ EPUB. המפרט עבור NCX פותח עבור ספר מדברים דיגיטלי (DTB) ופורמט קובץ זה נשמר על ידי **DAISY Consortium** ואינו חלק ממפרט EPUB. קובץ ה-NCX כולל בתוכו סוג פנטומימאי של **application/x-dtbncx+xml**.

## מפרט NCX ##

קובץ NCX מכיל סוגים שונים של תגי XML. המטא תגיות כמו `meta name="dtb:uid"` משמשים להזכרת המזהה. האלמנט `meta name="dtb:depth"` מוגדר שווה לעומק של רכיב התג `navMap`. ניתן לקנן את רכיבי 'navPoint' כדי ליצור תוכן עניינים היררכי. התוכן של `navLabel` הוא הטקסט המופיע בתוכן העניינים שנוצר על ידי מערכות קריאה המשתמשות ב-.ncx. התוכן של אלמנט `navPoint` מצביע על מסמך תוכן הרשום במניפסט ויכול לכלול גם מזהה אלמנט

תיאור של חריגים מסוימים למפרט NCX כפי שנמצא בשימוש ב-EPUB. כאן תוכל לצפות בדוגמה של קובץ NCX:

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

## הפניות ##

* [EPUB מוויקיפדיה](https://en.wikipedia.org/wiki/EPUB)
* [אילו קבצים לכלול ב-toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

