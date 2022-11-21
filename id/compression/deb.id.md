{
  "date" : "2021-04-08",
  "keywords" :[ "file deb", "format file deb", "apa itu file deb", "file", "contoh deb", "ekstensi file deb", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Arsip Tar Terkompresi Bzip",
  "description":"Pelajari tentang format file DEB dan API yang dapat membuat dan membuka file DEB.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Apa itu file DEB?

File dengan ekstensi .deb adalah format file paket biner Debian yang tersedia untuk distribusi paket perangkat lunak di OS Linux. Ini terdiri dari dua file arsip [TAR](/id/compression/tar/). DPKG menyediakan mekanisme untuk membaca dan menginstal paket DEB. Paket DEB dapat diinstal menggunakan antarmuka manajemen perangkat lunak paket APT. File DEB memiliki Internet Media Type sebagai `application/vnd.debian.binary-package`.

## Format File DEB

File DEB terdiri dari dua file arsip [TAR](/id/compression/tar/). Satu arsip menyimpan informasi kontrol dan arsip lainnya berisi data yang dapat diinstal.

### Organisasi Paket

File DEB adalah file arsip **ar** yang memiliki nilai ajaib `!<arch> `. Sejak Debian 0.93, mekanisme pengarsipan file DEB berisi tiga file dalam urutan tertentu.

1. `Debian Binary` - Ditakdirkan untuk memiliki serangkaian baris, dipisahkan oleh baris baru. Saat ini, hanya ada satu baris yang menjelaskan nomor versi. Nomor versi saat ini adalah 2.0.
1. `Control Archive` - Berisi arsip control.tar yang memiliki skrip pengelola dan informasi meta tentang paket seperti nama paket, versi, dependensi, dan pengelola.
1. `Arsip Data` - Ini adalah arsip tar bernama data.tar dan berisi file media aktual yang dapat diinstal. Arsip dapat dikompresi dengan gz, bz2, lzma atau xz, dan ekstensi file dari arsip data berubah sesuai dengan itu.

### Arsip Kontrol

Arsip kontrol dapat menyertakan konten sebagai berikut.

* `control` - Ini berisi deskripsi singkat tentang paket serta informasi lain seperti dependensinya.
* `md5sums` - Ini berisi checksum MD5 dari semua file dalam paket untuk mendeteksi file yang rusak atau tidak lengkap.
* `conffiles` - Daftar file paket yang harus diperlakukan sebagai file konfigurasi. File konfigurasi tidak ditimpa selama pembaruan kecuali ditentukan.
* `preinst`, postinst, prerm dan postrm - Skrip opsional yang dijalankan sebelum atau setelah menginstal atau menghapus paket
* `config` adalah skrip opsional yang mendukung mekanisme konfigurasi debconf.
* `shlibs` - Ini adalah daftar dependensi perpustakaan bersama.

## Referensi

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Format paket biner Debian](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

