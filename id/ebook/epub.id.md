{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "file", "extension", "format", "E-Book", "Digital book" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file EPUB dan API yang dapat membuat dan membuka file EPUB.",
  "title" :"Apa itu file EPUB?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Apa itu file EPUB?

File dengan ekstensi .epub adalah format file e-book yang menyediakan format publikasi digital standar untuk penerbit dan konsumen. Formatnya sudah sangat umum sekarang sehingga didukung oleh banyak e-reader dan aplikasi perangkat lunak. Misalnya, di Mac OS, perangkat lunak **Books** prainstal menyediakan dukungan untuk membuka file semacam itu. Selain itu, ada banyak perangkat lunak yang kompatibel tersedia untuk ponsel cerdas, tablet, dan komputer. Standar file EPUB dikelola oleh [International Digital Publishing Forum ](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). Versi EPUB 3 juga didukung oleh Book Industry Study Group (BISG), sebuah asosiasi perdagangan buku terkemuka untuk standar praktik terbaik, penelitian, informasi dan acara, untuk pengemasan konten.

## Sejarah Singkat Format File EPUB

* **Oktober 2007** - EPUB 2.0 disetujui
* **September 2010** - Pembaruan pemeliharaan dirilis
* **Oktober 2011** - Spesifikasi EPUB 3.0 menjadi efektif
* **Juni 2014** - Pembaruan pemeliharaan kecil dirilis untuk menggantikan versi 3.0
* **Januari 2017** - EPUB 3.1 mulai berlaku

## Format File EPUB

Format file EPUB adalah arsip yang dapat diubah namanya menjadi ekstensi [ZIP](/id/compression/zip/) dan isinya dapat dilihat dengan mengekstrak arsip dengan ekstraktor arsip apa pun. Ini adalah format berbasis XML terbuka dan terdiri dari file HTML, gambar, lembar gaya CSS, dan elemen lainnya. Itu juga dapat dikonversi ke PDF, Mobi dan beberapa format file lainnya melalui sejumlah aplikasi perangkat lunak dan API.

{{< figure src="../epub.png" alt="Format File EPUB" >}}

**E-Book EPUB dibuka dengan Aplikasi Mac OS Books**

Format file EPUB didasarkan pada tiga standar terbuka berikut.

### Struktur Publik Terbuka (OPS) ###

File EPUB 2.0 menggunakan XHTML 1.1 untuk membuat konten publikasi. Intinya ini berarti file EPUB terdiri dari satu atau lebih halaman web. Meskipun Anda dapat menyertakan seluruh konten buku atau surat kabar dalam satu halaman, sebaiknya file tersebut tidak melebihi 300K, baik untuk alasan kinerja maupun kompatibilitas. Sama seperti halaman web biasa, gaya dan tata letak ditentukan menggunakan cascading style sheets (CSS). Dalam file EPUB, subset (serangkaian perintah terbatas) dari CSS2 perlu digunakan. Banyak fitur baru CSS3, seperti kotak bulat atau bayangan, belum tersedia. Untuk kompatibilitas mundur, kreator juga dapat menggunakan DTBook alih-alih XHTML untuk menyandikan konten.

### Format Kemasan Terbuka (OPF) ###

Bagian spesifikasi ini berkaitan dengan informasi struktural seperti metadata (siapa penulis dan penerbit, apa judulnya,..), manifes (daftar semua file di dalam file epub) dan daftar isi. Semua data ini disematkan menggunakan XML.

### Format Wadah Terbuka (OCF) ###

Seperti uraian di atas seharusnya menjelaskan bahwa dokumen EPUB terdiri dari serangkaian file. Spesifikasi OCF menentukan bagaimana semua file tersebut akhirnya dikemas dalam satu file kontainer tunggal. Kompresi ZIP digunakan untuk ini.

## Format File Gambar yang Didukung ##

Format file EPUB mendukung format file gambar berikut.

* [GIF](/id/image/gif/)
* [JPG](/id/image/jpeg/)
* [PNG](/id/image/png/)
* [SVG](/id/page-description-language/svg/)

## Referensi ##

* [EPUB - Oleh Wikipedia](https://en.wikipedia.org/wiki/EPUB)

