{
  "date" : "2019-10-11",
  "keywords" :[ "file tar", "format file tar", "apa itu file tar", "file", "contoh tar", "ekstensi file tar", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Format File Arsip Unix",
  "description":"Pelajari tentang apa itu file Tar dan API yang dapat membuat dan membuka file TAR.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file TAR?

File dengan ekstensi .tar adalah arsip yang dibuat dengan utilitas berbasis Unix untuk mengumpulkan satu atau lebih file. Banyak file disimpan dalam format yang tidak terkompresi dengan dukungan penambahan file serta folder ke arsip. Utilitas TAR di Unix berbasis Perintah, tetapi file yang dibuat didukung oleh sebagian besar sistem pengarsipan file di hampir semua sistem operasi. Ini pertama kali dibuat pada tahun 1979 oleh AT&T Bell Laboratories dan versi selanjutnya diterbitkan seiring berjalannya waktu.

## Format File TAR

TAR adalah format file terbuka dengan spesifikasi lengkap yang tersedia untuk referensi pengembang. Struktur filenya distandarisasi di POSIX.1-1988 dan kemudian di POSIX.1-2001. Kumpulan data yang dibuat oleh tar menyimpan informasi tentang parameter sistem file seperti:

* Nama
* Stempel Waktu
* Kepemilikan
* Izin Akses File
* Organisasi Direktori

File Tar tidak memiliki angka ajaib. Ini berisi serangkaian blok di mana setiap blok adalah byte BLOCKSIZE.

Setiap file yang diarsipkan diwakili oleh blok header yang menjelaskan file, diikuti oleh nol atau lebih blok yang memberikan isi file. Di akhir file arsip terdapat dua blok berukuran 512 byte yang diisi dengan angka nol biner sebagai penanda akhir file. Sistem yang masuk akal harus menulis penanda akhir file seperti itu di akhir arsip, tetapi tidak boleh berasumsi bahwa blok seperti itu ada saat membaca arsip. Khususnya tar GNU selalu mengeluarkan peringatan jika tidak menemukannya.

Blok mungkin diblokir untuk operasi I/O fisik. Setiap record n blok (di mana n diatur oleh opsi blocking-factor = 512-size ke tar) ditulis dengan satu operasi "write()". Pada pita magnetik, hasil penulisan seperti itu adalah satu rekaman. Saat menulis arsip, catatan blok terakhir harus ditulis dalam ukuran penuh, dengan blok setelah blok nol berisi semua nol. Saat membaca arsip, sistem yang masuk akal harus menangani arsip dengan benar yang catatan terakhirnya lebih pendek dari yang lain, atau yang berisi catatan sampah setelah blok nol.

### Tajuk Tar

Seperti header file lainnya, rekaman header file tar berisi metadata tentang file dan ditampilkan dalam tabel berikut.


|Offset bidang|Ukuran bidang (Byte)|Bidang
---|---|---|
|0|100|Nama berkas
|100|8|Mode berkas
|108|8|ID pengguna numerik pemilik
|116|8|ID pengguna numerik grup
|124|12|Ukuran file dalam byte (basis oktal)
|136|12|Waktu modifikasi terakhir dalam format waktu numerik Unix (oktal)
|148|8|Checksum untuk rekaman tajuk
|156|1|Indikator tautan (tipe file)
|157|100|Nama file tertaut

Bidang yang tidak digunakan diisi dengan byte NUL. Header terdiri dari 257 byte yang diisi dengan byte NUL untuk membuatnya mengisi catatan 512 byte.

## Referensi ##

* [TAR - Oleh Wikipedia](https://en.wikipedia.org/wiki/Tar_(computing))
* [Format Dasar TAR](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

