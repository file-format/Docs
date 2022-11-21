{
  "date" : "2021-04-08",
  "keywords" :[ "file dar", "format file dar", "apa itu file dar", "file", "contoh dar", "ekstensi file dar", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Format File Pengarsip Disk",
  "description":"Pelajari tentang format file DAR dan API yang dapat membuat dan membuka file DAR.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Apa itu file DAR?

File dengan ekstensi .dar adalah arsip terkompresi yang dibuat menggunakan arsip DAR Disk. Itu dapat membuat cadangan / arsip untuk disk penuh atau sekelompok file. Itu dibuat untuk menggantikan format file [TAR](/id/compression/tar/) pada OS UNIX dan dapat dibuat sebagai file arsip terpisah untuk sejumlah besar file. Arsip DAR mendukung opsi untuk menghapus file dari sistem yang ditautkan ke file utama dalam arsip. Kemampuannya dalam menyediakan cadangan diferensial, Inkremental, dan Penurunan membuatnya lebih unggul daripada file TAR.

## Format File DAR

File DAR adalah arsip terkompresi yang dapat menggunakan kompresi per file seperti [gzip](/id/compression/gz/), [bzip2](/id/compression/bz2/), lzo, xz, atau lzma. Format file yang tepat dari file DAR bergantung pada jenis pemformatan yang digunakan untuk mengompresi konten arsip. Ini juga memungkinkan enkripsi Blowfish, Twofish, AES, Serpent, Camellia opsional, dan enkripsi dan tanda tangan kunci publik (OpenPGP).

### Fitur DAR

Beberapa fitur format file DAR adalah sebagai berikut.

* Menangani semua jenis inode (direktori, file biasa, symlink, perangkat khusus, pipa bernama, soket, pintu, ...)
* Menjaga inode yang ditautkan dengan keras (file biasa yang ditautkan dengan keras, perangkat char, perangkat blok, symlink yang ditautkan dengan keras)
* Mengurus file jarang
* Mengurus file Linux Extended Attributes,
* Mengurus ACL file Linux
* Mengurus garpu file Mac OS X
* Menangani beberapa atribut khusus sistem file seperti Tanggal lahir sistem file HFS+ dan atribut tidak berubah, penjurnalan data, penghapusan aman, penggabungan tanpa ekor, tidak dapat dihapus, noatime dari sistem file ext2/3/4.
* Kompresi per file dengan gzip, bzip2, lzo, xz atau lzma (berlawanan dengan mengompresi seluruh arsip). Seseorang dapat memilih untuk tidak mengompres file yang sudah dikompresi berdasarkan akhiran nama file mereka.
* Mengekstraksi file dengan cepat dari mana saja di arsip
* Daftar cepat isi arsip dengan menyimpan katalog file dalam arsip
* Cadangan sistem file langsung: mendeteksi ketika file telah dimodifikasi saat sedang dibaca untuk cadangan dan dapat mencoba lagi menyimpannya hingga jumlah percobaan ulang maksimum yang diberikan
* File hash (MD5, SHA1 atau SHA-512) dihasilkan on-fly untuk setiap irisan, file yang dihasilkan kompatibel dengan md5sum atau sha1sum, untuk dapat dengan cepat memeriksa integritas setiap irisan
* Filesystem independen: dapat digunakan untuk memulihkan sistem ke partisi dengan ukuran yang berbeda dan/atau ke partisi dengan sistem file yang berbeda[5]

## Referensi

* [DAR](http://dar.linux.free.fr/)
* [Pengarsipan Disk DAR](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

