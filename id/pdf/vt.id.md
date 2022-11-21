{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File PDF/VT",
  "description":"Pelajari tentang format file PDF/VT dan API yang dapat membuat dan membuka file PDF/VT.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Apa itu PDF/VT? #

PDF/VT, diterbitkan sebagai [ISO 16612-2](https://www.iso.org/standard/46428.html) pada Agustus 2010 sebagai standar, dirancang untuk memungkinkan pencetakan dokumen variabel (VDP) dalam berbagai lingkungan. Standar menjadikan informasi Variabel dan pencetakan Transaksional sebagai dasar standarnya. Pencetakan data Variabel digunakan di mana bagian informasi berbeda untuk setiap penerima konten. Pencetakan Transaksional mencakup faktur, pernyataan, dan dokumen lain yang menggabungkan informasi penagihan dengan informasi pemasaran. Ini menghasilkan campuran pemrosesan gambar, teks, dan jenis konten lainnya yang lebih baik. PDF/VT memungkinkan pengelolaan halaman yang andal dan dinamis untuk data cetak High Volume Transactional Output (HVTO) dengan menggunakan konsep metadata bagian dokumen (DPM). File PDF/VT dapat dibuka di Adobe Acrobat viewer tanpa perlu menambahkan komponen lain.

## Hirarki Bagian Dokumen ##

Hierarki Bagian Dokumen (DPart) seperti struktur pohon node bagian dokumen yang didasarkan pada semua halaman dalam dokumen. Elemen pohon ini disebut node DPart. Setiap simpul internal berisi simpul DPart lainnya dan setiap simpul daun menentukan satu atau lebih halaman untuk penerima. Pada dasarnya, hierarki DPart menentukan urutan dan hubungan dokumen atau kumpulan dokumen dalam file PDF/VT. Struktur pohon simpul DPart mewakili konten internal dokumen PDF/VT dengan mudah karena mungkin berisi sub-dokumen untuk banyak penerima dan setiap bagian dokumen sesuai dengan halaman untuk satu penerima. Hierarki DPart diperlukan dalam file PDF/VT.

## Metadata Bagian Dokumen (DPM) ##

Metadata Bagian Dokumen (DPM) dikaitkan dengan setiap node dalam hierarki bagian dokumen dan dapat digunakan untuk mengomunikasikan informasi tentang subdokumen penerima tertentu dan bagian-bagiannya. Secara khusus, DPM dapat berisi informasi tentang properti atau informasi tentang penerima dalam bentuk yang disandikan.

## Tingkat Kesesuaian ##

PDF/VT diberikan pada tiga tingkat kesesuaian berikut. Ini semua berdasarkan [PDF](/id/pdf/) 1.6.

* `PDF/VT-1` - Ini didasarkan pada PDF/X-4 dan berisi semua sumber daya yang diperlukan untuk merender dokumen PDF.
* `PDF/VT-2` - Dirancang untuk pertukaran multi-file, dokumen PDF/VT-2 dapat merujuk maksud output eksternal, konten eksternal, atau keduanya. Dokumen PDF/VT dan semua file PDF yang direferensikan serta maksud keluaran eksternal secara kolektif disebut kumpulan file PDF/VT-2. Acrobat 9 dan mendukung fitur ini.
* `PDF/VT-2s` - Mendukung streaming langsung PDF/VT-2. Ini memungkinkan bagian data yang tersegmentasi untuk diproses.

## Referensi ##

* [PDF/VT - Dari Wikipedia](https://en.wikipedia.org/wiki/PDF/VT)
* [ISO 16612-2 Teknologi Grafis](https://www.iso.org/standard/46428.html)

