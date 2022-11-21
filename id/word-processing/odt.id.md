{
  "date" : "2019-10-11",
  "keywords" :[ "file odt", "format file odt", "apa itu file odt", "file", "contoh odt", "ekstensi file odt", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODT - File Teks OpenDocument",
  "description":"Pelajari tentang format file ODT dan API yang dapat membuat dan membuka file ODT.",
  "linktitle" : "ODT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file ODT?

File ODT adalah jenis dokumen yang dibuat dengan aplikasi pengolah kata yang didasarkan pada format File Teks OpenDocument. Ini dibuat dengan aplikasi pengolah kata seperti OpenOffice Writer gratis dan dapat menampung konten seperti teks, gambar, objek, dan gaya. File ODT adalah untuk pengolah kata Writer seperti [DOCX](/id/pemrosesan kata/docx/) untuk Microsoft Word. Beberapa aplikasi termasuk Google Docs dan pengolah kata berbasis web Google yang disertakan dengan Google Drive dapat membuka file ODT untuk diedit. Microsoft Word juga dapat membuka file ODT dan menyimpannya dalam format lain seperti [DOC](/id/word-processing/doc/) dan DOCX.

## Sejarah Singkat ##

Spesifikasi format file ODP didasarkan pada standar yang dikembangkan sebagai spesifikasi ODF. Spesifikasi ini telah berkembang selama ini dalam bentuk tiga versi yang dikembangkan dan diterbitkan oleh OASIS sebagai berikut:

**2005** Versi 1.0 diterbitkan pada Mei 2005

**2007:** Versi 1.1 diterbitkan pada Februari 2007

**2011:** Versi 1.2 diterbitkan pada Sep 2011

Ada sedikit perubahan dalam transisi dari versi ODF 1.0 ke 1.1. [Versi ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) adalah versi terbaru untuk spesifikasi ODF dan harus dikonsultasikan dengan pengembang untuk pengembangan aplikasi yang terkait dengan pembacaan/penulisan ODS.

## Spesifikasi Format File ##

Format OpenDocument mendukung representasi dokumen sebagai satu dokumen XML serta kumpulan beberapa subdokumen dalam sebuah paket sebagai arsip [ZIP](/id/Compression/ZIP/). Setiap file dari arsip ZIP menyimpan sebagian dari dokumen lengkap. Setiap subdokumen menyimpan aspek tertentu dari dokumen. Misalnya, satu subdokumen berisi informasi gaya dan subdokumen lainnya berisi konten dokumen. Dokumen ODF tipikal memiliki komponen berikut:

* content.xml – Konten dokumen dan gaya otomatis yang digunakan dalam konten.
* styles.xml – Gaya yang digunakan dalam konten dokumen dan gaya otomatis yang digunakan dalam gaya itu sendiri.
* meta.xml – Mendokumentasikan informasi meta, seperti pembuat atau waktu penyimpanan terakhir.
* settings.xml – Pengaturan khusus aplikasi, seperti ukuran jendela atau informasi printer.

Selain itu, dalam paket bisa ada banyak subdokumen lain seperti thumbnail dokumen, gambar, dll. File dokumen adalah subset dari file ODF tempat konten (lembar) disimpan di //content.xml// subdokumen.

## Referensi ##

* [OpenDocument - Oleh Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

