{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "File XML Kontrol Navigasi EPUB", "ekstensi", "format", "Buku Elektronik", "TOC", "Konsorsium DAISY"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file EPUB Navigation Control XML File(NCX) dan API yang dapat membuat dan membuka file NCX.",
  "title" :"NCX - File XML Kontrol Navigasi EPUB",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Apa itu file NCX? ##

File NCX disingkat sebagai file Kontrol Navigasi untuk XML, biasanya bernama toc.ncx. File ini terdiri dari daftar isi hierarkis untuk file EPUB. Spesifikasi NCX dikembangkan untuk Digital Talking Book (DTB) dan format file ini dikelola oleh **DAISY Consortium** dan bukan bagian dari spesifikasi EPUB. File NCX menyertakan jenis mime dari **application/x-dtbncx+xml** ke dalamnya.

## Spesifikasi NCX ##

File NCX berisi berbagai macam tag XML. Tag meta seperti `meta name="dtb:uid"` digunakan untuk menyebutkan ID. Elemen `meta name="dtb:depth"` disetel sama dengan kedalaman elemen tag `navMap`. Elemen `navPoint` dapat disarangkan untuk membuat daftar isi yang hierarkis. Konten `navLabel` adalah teks yang muncul di daftar isi yang dihasilkan oleh sistem pembacaan yang menggunakan .ncx. Konten elemen `navPoint` mengarah ke dokumen konten yang tercantum dalam manifes dan juga dapat menyertakan pengidentifikasi elemen

Deskripsi pengecualian tertentu pada spesifikasi NCX seperti yang digunakan dalam EPUB. Di sini Anda dapat melihat contoh file NCX:

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

## Referensi ##

* [EPUB Dari Wikipedia](https://en.wikipedia.org/wiki/EPUB)
* [File apa yang akan disertakan dalam toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

