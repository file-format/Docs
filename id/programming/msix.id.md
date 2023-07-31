{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - Apa itu file MSIX?",
  "description":"Pelajari tentang file MSIX dan API yang dapat membuat dan membuka file MSIX.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Apa itu file MSIX?

File MSIX adalah format pengemasan aplikasi Windows yang digunakan untuk membuat dan mendistribusikan aplikasi di Windows 10. Ini adalah format file paket modern dibandingkan dengan [APPX](/id/programming/appx/) dan MSI yang akhirnya akan dihapus ke format file baru ini. Ini dapat digunakan untuk penyebaran aplikasi Win32, WPF, dan Windows Forms. File MSIX dapat diandalkan, dan menargetkan jaringan dan pengoptimalan ruang disk. Pengembang menggunakan ini untuk mendistribusikan program ke pengguna akhir melalui Microsoft Store (sebelumnya dikenal sebagai Windows Store).

## Format File MSIX - Informasi Lebih Lanjut

File MSIX dikompresi [ZIP](/id/compression/zip/), dengan semua file disertakan di dalam file paket. Selain file terkait aplikasi, file MSIX berisi file konfigurasi [.xml](/id/web/xml/) yang berisi informasi terkait penginstalan aplikasi.

## Apa yang ada di dalam paket MSIX?

Paket MSIX terdiri dari file-file berikut.

* `AppxBlockMap.xml` - Dikenal sebagai file peta blok paket, ini adalah dokumen XML yang berisi daftar file aplikasi dengan indeks dan hash kriptografis untuk setiap blok data yang disimpan dalam paket.
* `AppxManifest.xml` - Dokumen XML yang berisi informasi yang diperlukan untuk penerapan, tampilan, dan pembaruan aplikasi MSIX. Info ini mencakup identitas paket, dependensi paket, kemampuan yang diperlukan, elemen visual, dan poin ekstensibilitas.
* `AppxSignature.p7x` - File yang dibuat saat paket ditandatangani. Semua paket MSIX harus ditandatangani sebelum menginstal. Dengan AppxBlockmap.xml, platform dapat menginstal paket dan divalidasi.

## Referensi

* [Ikhtisar MSIX](https://learn.microsoft.com/en-us/windows/msix/overview)
* [Buat file APPX menggunakan Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

