{
  "date" : "2019-10-11",
  "keywords" :[ "file odp", "format file odp", "apa itu file odp", "file", "contoh odp", "ekstensi file odp", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - Format File Presentasi OpenOffice",
  "description":"Pelajari tentang format file ODP dan API yang dapat membuat dan membuka file ODP.",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file ODP?

File dengan ekstensi .odp mewakili format file presentasi yang digunakan oleh OpenOffice.org dalam standar OASISOpen. File presentasi adalah kumpulan slide di mana setiap slide dapat terdiri dari teks, gambar, format, animasi, dan media lainnya. Slide ini disajikan kepada audiens dalam bentuk tayangan slide dengan pengaturan presentasi khusus. File ODP dapat dibuka oleh aplikasi yang sesuai dengan format OpenDocument (seperti OpenOffice atau StarOffice).

## Sejarah Singkat

Spesifikasi format file ODP didasarkan pada standar yang dikembangkan sebagai spesifikasi ODF. Spesifikasi ini telah berkembang selama ini dalam bentuk tiga versi yang dikembangkan dan diterbitkan oleh OASIS sebagai berikut:

`2005` - Versi 1.0 diterbitkan pada Mei 2005
`2007` - Versi 1.1 diterbitkan pada Februari 2007
`2011` - Versi 1.2 diterbitkan pada Sep 2011

Ada sedikit perubahan dalam transisi dari versi ODF 1.0 ke 1.1. [Versi ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) adalah versi terbaru untuk spesifikasi ODF dan harus dikonsultasikan dengan pengembang untuk pengembangan aplikasi yang terkait dengan pembacaan/penulisan ODS.

## Spesifikasi Format File

Format OpenDocument mendukung representasi dokumen sebagai satu dokumen XML serta kumpulan beberapa subdokumen dalam sebuah paket sebagai arsip [ZIP](https://docs.fileformat.com/Compression/ZIP/). Setiap file dari arsip ZIP menyimpan sebagian dari dokumen lengkap. Setiap subdokumen menyimpan aspek tertentu dari dokumen. Misalnya, satu subdokumen berisi informasi gaya dan subdokumen lainnya berisi konten dokumen. Dokumen ODF tipikal memiliki komponen berikut:

* `content.xml` – Konten dokumen dan gaya otomatis yang digunakan dalam konten.
* `styles.xml` – Gaya yang digunakan dalam konten dokumen dan gaya otomatis yang digunakan dalam gaya itu sendiri.
* `meta.xml` – Mendokumentasikan informasi meta, seperti penulis atau waktu penyimpanan terakhir.
* `settings.xml` – Pengaturan khusus aplikasi, seperti ukuran jendela atau informasi printer.

Selain itu, dalam paket bisa ada banyak subdokumen lain seperti thumbnail dokumen, gambar, dll.

File dokumen spreadsheet adalah subset dari file ODF tempat konten (sheet) disimpan di subdokumen content.xml.

## Referensi

* [OpenDocument - Oleh Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

