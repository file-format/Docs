{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "file", "ekstensi", "format file", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file OTS dan API yang dapat membuat dan membuka file OTS.",
  "title" :"OTS - Format File Templat Spreadsheet OpenDocument",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Apa itu file OTS?

File dengan ekstensi .ots adalah file Templat OpenDocument Spreadsheet yang dibuat dengan perangkat lunak aplikasi Calc yang termasuk dalam Apache OpenOffice. Perangkat lunak aplikasi Calc mirip dengan Excel yang tersedia di Microsoft Office. Format file OTS digunakan untuk membuat template yang berisi pengaturan yang telah ditentukan sebelumnya terkait dengan gaya, font, data, tata letak spreadsheet, dan pemformatan. File OTF memiliki `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. File template ini dapat digunakan sebagai titik awal untuk membuat dan menyimpan file data aktual yang disimpan dalam [format file ODS](/id/spreadsheet/ods/). File OTS dapat digunakan dengan aplikasi seperti OpenOffice dan LibreOffice.

## Format File OT

File OTS disimpan dalam format file berbasis XML OpenDocument OASIS yang terdiri dari kumpulan beberapa subdokumen dengan paket sebagai arsip [ZIP](/id/compression/zip/). Setiap arsip zip menyimpan bagian dari dokumen lengkap dan setiap subdokumen menyimpan aspek tertentu dari dokumen tersebut. Misalnya, satu subdokumen berisi informasi gaya dan subdokumen lainnya berisi konten dokumen. Dokumen ODF tipikal memiliki komponen berikut:

### Konten OTS.xml

File content.xml berisi konten dokumen yang sebenarnya. Namun, ini tidak termasuk data biner seperti gambar.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml dari Format Berkas OTS

File styles.xml berisi informasi gaya dan banyak digunakan untuk pemformatan dan tata letak. Jenis gaya meliputi:

* Gaya paragraf
* Gaya halaman
* Gaya karakter
* Gaya bingkai
* Daftar gaya

### Meta.xml

File meta.xml berisi informasi tentang metadata file seperti Penulis, Tanggal Modifikasi Terakhir, dll.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Pengaturan.xml

File `settings.xml` mencakup pengaturan tingkat dokumen seperti faktor zoom dan posisi kursor.

## Referensi ##

* [Spesifikasi OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - Oleh Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

