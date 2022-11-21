{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "file", "extension", "file format", "OpenDocument Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Panduan format file Anda untuk mengetahui apa itu file ODS dan API yang dapat membuat dan membukanya.",
  "title" :"Apa itu file ODS?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Apa itu file ODS?

File dengan ekstensi .ods adalah format Dokumen OpenDocument Spreadsheet yang dapat diedit oleh pengguna. Data disimpan di dalam file ODF ke dalam baris dan kolom. Ini adalah format berbasis XML dan merupakan salah satu dari beberapa subtipe dalam keluarga Open Document Formats (ODF). Format ditentukan sebagai bagian dari spesifikasi ODF 1.2 yang diterbitkan dan dikelola oleh OASIS. Sejumlah aplikasi di Windows serta sistem operasi lain dapat membuka file ODS untuk diedit dan dimanipulasi termasuk Microsoft Excel, NeoOffice, dan LibreOffice. File ODS juga dapat dikonversi ke format spreadsheet lain seperti [XLS](/id/spreadsheet/xls/), [XLSX](/id/spreadsheet/xlsx/) dan lainnya dengan aplikasi yang berbeda.

## Sejarah Singkat ##

Spesifikasi format file ODS didasarkan pada standar yang dikembangkan sebagai spesifikasi ODF. Spesifikasi ini telah berkembang selama ini dalam bentuk tiga versi yang dikembangkan dan diterbitkan oleh OASIS sebagai berikut:

`2005`- Versi 1.0 diterbitkan pada Mei 2005

`2007` - Versi 1.1 diterbitkan pada Februari 2007

`2011` - Versi 1.2 diterbitkan pada Sep 2011

Ada sedikit perubahan dalam transisi dari versi ODF 1.0 ke 1.1. [Versi ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) adalah versi terbaru untuk spesifikasi ODF dan harus dikonsultasikan dengan pengembang untuk pengembangan aplikasi yang terkait dengan pembacaan/penulisan ODS.

## Format File ODS ##

Format OpenDocument mendukung representasi dokumen sebagai satu dokumen XML serta kumpulan beberapa subdokumen dalam sebuah paket sebagai arsip [ZIP](/id/compression/zip/). Setiap file dari arsip ZIP menyimpan sebagian dari dokumen lengkap. Setiap subdokumen menyimpan aspek tertentu dari dokumen. Misalnya, satu subdokumen berisi informasi gaya dan subdokumen lainnya berisi konten dokumen. Dokumen ODF tipikal memiliki komponen berikut:

* `content.xml` – Konten dokumen dan gaya otomatis yang digunakan dalam konten.
* `styles.xml` – Gaya yang digunakan dalam konten dokumen dan gaya otomatis yang digunakan dalam gaya itu sendiri.
* `meta.xml` – Mendokumentasikan informasi meta, seperti penulis atau waktu penyimpanan terakhir.
* `settings.xml` – Pengaturan khusus aplikasi, seperti ukuran jendela atau informasi printer.

Selain itu, dalam paket bisa ada banyak subdokumen lain seperti thumbnail dokumen, gambar, dll.

File dokumen spreadsheet adalah subset dari file ODF tempat konten (sheet) disimpan di subdokumen content.xml.

## Referensi ##

* [OpenDocument - Oleh Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

