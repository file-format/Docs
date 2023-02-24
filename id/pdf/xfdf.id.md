{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File XFDF - Apa itu file XFDF?",
  "description":"Pelajari tentang file XFDF dan API yang dapat membuat dan membuka file XFDF.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file XFDF?

File dengan ekstensi .xfdf adalah Format Data Formulir XML yang dibuat dengan perangkat lunak Adobe Acrobat. Seperti [FDF](/id/pdf/fdf/), XFDF berisi deskripsi elemen formulir dan nilainya dalam format XML. Ini dapat menyertakan nama dan nilai bidang teks dalam formulir PDF. XFDF disimpan dalam format yang dapat dibaca manusia dan dapat dibaca secara terprogram menggunakan bahasa pemrograman seperti C#.

## Format File XFDF - Informasi Lebih Lanjut

File XFDF disimpan dalam format file XML yang merupakan format universal yang digunakan untuk mengimpor dan mengekspor data. Struktur file XFDF terdiri dari header, diikuti dengan nilai bidang, dan data elemen seperti yang ditunjukkan di bawah ini.

|Elemen|Atribut|Konten|
---|---|---|
|\<XFDF> ||Elemen paling atas|
|\<fields> ||Semua nilai bidang untuk templat ini|
|<field (T)> |nama |Nama medan|
|<value (V)> |nilai |Nilai bidang|

## Referensi

* [Dukungan Format FDF oleh Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Sumber Daya Pengembang Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

