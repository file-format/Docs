{
  "date" : "2019-12-09",
  "keywords" :[ "file zip", "format file zip", "apa itu file zip", "file", "contoh zip", "ekstensi file zip", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RITSLETING",
  "description":"Apa itu file ZIP dan API yang dapat membuat dan membuka file ZIP.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Apa itu file ZIP? ##

File dengan ekstensi .zip adalah arsip yang dapat menampung satu atau lebih file atau direktori. Arsip dapat memiliki kompresi yang diterapkan pada file yang disertakan untuk mengurangi ukuran file ZIP. Format file ZIP dipublikasikan kembali pada Februari 1989 oleh Phil Katz untuk mencapai pengarsipan file dan folder. Format tersebut dijadikan bagian dari utilitas [PKZIP](https://www.pkware.com/pkzip), yang dibuat oleh PKWARE, Inc. Tepat setelah ketersediaan [spesifikasi yang tersedia](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), banyak perusahaan menjadikan format file ZIP sebagai bagian dari utilitas perangkat lunak mereka termasuk Microsoft (sejak Windows 7), Apple (Mac OS X) dan banyak lainnya.

## Sejarah Singkat Format File ZIP

Sejarah format file ZIP berawal dari peristiwa tuntutan hukum yang diajukan oleh System Enhancement Associates (SEA) terhadap PKWARE karena menggunakan utilitas ARC tanpa izin untuk merek dagangnya dan hak cipta atas tampilan produk dan antarmuka pengguna. Sebelumnya, Phil Katz, telah menulis ulang kode sumber SEA dan merilis PKXARC, sebuah ekstraktor ARC, dan PKARC, sebuah kompresor file, sebagai freeware untuk sistem berbasis MS-DOS. Kalah dari tuntutan hukum, PKWARE tidak bisa menggunakan apapun yang berhubungan dengan ARC lagi. Di sinilah pembuatan kompresi file baru muncul, dinamai ZIP yang dijadikan bagian dari utilitas PKZIP di PKWARE, Inc.

Katz merilis spesifikasi format file ZIP ke dalam domain publik, sambil mempertahankan hak kepemilikan atas utilitas kompresi dan ekstraksinya yaitu PKZIP. Sistem kompresi ZIP telah (dan) dapat mengarsipkan file dalam folder melalui algoritma 32-bit cyclic redundancy check ([CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)) untuk mengompres file ukuran. Tidak seperti ARC, folder .ZIP menyertakan file direktori yang berperan sebagai buku kode kriptografer, menyimpan informasi yang diperlukan untuk merender file terkompresi.

## Metode Kompresi yang Didukung dalam ZIP

Sesuai spesifikasi Format File .ZIP, metode kompresi berikut ini didukung.

* Store - berarti tidak ada kompresi
* Menyusut
* Pengurangan (Ini menyiratkan faktor kompresi mulai dari level 1 hingga level 4)
* Meledak
* Mengempis
* Deflat64
* BZIP2
* LZMA (EFS)
* Paket Wav
* PPMd versi I, Rev 1

DEFLATE adalah metode kompresi yang umum digunakan yang merupakan algoritme kompresi tanggal lossless yang menggunakan kombinasi pengkodean LZ77 dan Huffman dan dirinci dalam [RFC 1951](https://tools.ietf.org/html/rfc1951).

## Spesifikasi Format File ZIP

File ZIP memiliki kemampuan untuk menyimpan banyak file menggunakan teknik kompresi yang berbeda sementara pada saat yang sama mendukung penyimpanan file tanpa kompresi apa pun. Setiap file disimpan/dikompresi secara individual yang membantu mengekstraknya, atau menambahkan yang baru, tanpa menerapkan kompresi atau dekompresi ke seluruh arsip.

### Keseluruhan Format File ZIP

Setiap file Zip disusun dengan cara berikut:


| Format File ZIP
---|
|Tajuk Berkas Lokal 1
|Berkas Data 1
|Deskriptor Data 1
|Tajuk Berkas Lokal 2
|Berkas Data 2
| Deskriptor Data 2
| ....
| ....
|Tajuk Berkas Lokal N
|Berkas Data N
|Deskriptor Data N
| Header Dekripsi Arsip
|Arsipkan Rekaman Data Ekstra
| Direktori Pusat

Format file ZIP menggunakan algoritma CRC 32-bit untuk tujuan pengarsipan. Untuk merender file terkompresi, arsip ZIP menyimpan direktori di ujungnya yang menyimpan entri file yang terkandung dan lokasinya di file arsip. Dengan demikian, memainkan peran pengkodean untuk mengenkapsulasi informasi yang diperlukan untuk membuat file terkompresi. Pembaca ZIP menggunakan direktori untuk memuat daftar file tanpa membaca seluruh arsip ZIP. Formatnya menyimpan salinan ganda dari struktur direktori untuk memberikan perlindungan yang lebih besar terhadap kehilangan data.

Setiap file dalam arsip ZIP direpresentasikan sebagai entri individu di mana setiap entri terdiri dari Header File Lokal diikuti oleh data file terkompresi. Direktori di akhir arsip menyimpan referensi ke semua entri file ini. Pembaca file ZIP harus menghindari membaca header file lokal dan semua jenis daftar file harus dibaca dari Direktori. Direktori ini adalah satu-satunya sumber untuk entri file yang valid dalam arsip karena file juga dapat ditambahkan menjelang akhir arsip. Itu sebabnya jika pembaca membaca tajuk lokal arsip ZIP dari awal, ia mungkin membaca entri yang tidak valid (dihapus) juga yang bukan bagian dari Direktori yang dihapus dari arsip.

Urutan entri file di direktori pusat tidak perlu sama dengan urutan entri file di arsip.

### Entri Berkas ZIP

Entri dalam file ZIP disusun satu demi satu dimana setiap entri terdiri dari:

* Tajuk Berkas Lokal
* Bidang Data Ekstra Opsional
* Data pengguna (opsional dikompresi/opsional dienkripsi)

Header File Lokal dari setiap entri mewakili informasi tentang file seperti komentar, ukuran file, dan nama file. Bidang data tambahan (opsional) dapat menampung informasi untuk opsi ekstensibilitas format ZIP.

#### Header Berkas Lokal

Header File Lokal memiliki struktur bidang khusus yang terdiri dari nilai multi-byte. Semua nilai disimpan dalam urutan byte little-endian di mana panjang bidang menghitung panjang dalam byte. Semua struktur dalam file ZIP menggunakan tanda tangan 4-byte untuk setiap entri file. Akhir dari tanda tangan direktori pusat adalah 0x06054b50 dan dapat dibedakan menggunakan tanda tangan uniknya sendiri. Berikut urutan informasi yang tersimpan di Local File Header.


|Offset|Bytes|Deskripsi
---|---|---|
|0|4|Tanda tangan header file lokal # 0x04034b50 (dibaca sebagai angka little-endian)
|4|2|Versi diperlukan untuk mengekstrak (minimum)
|6|2|Bendera tujuan umum bit
|8|2|Metode kompresi
|10|2|File waktu modifikasi terakhir
|12|2|File tanggal modifikasi terakhir
|14|4|CRC-32
|18|4|Ukuran terkompresi
|22|4|Ukuran tidak terkompresi
|26|2|Panjang nama berkas (n)
|28|2|Panjang bidang ekstra (m)
|30|n|Nama Berkas
|30+n|m|Bidang Ekstra

#### Header Berkas Direktori Pusat


|Offset|Bytes|Deskripsi
---|---|---|
|0|4|Tanda tangan tajuk file direktori pusat # 0x02014b50
|4|2|Versi dibuat oleh
|6|2|Versi diperlukan untuk mengekstrak (minimum)
|8|2|Bendera tujuan umum bit
|10|2|Metode kompresi
|12|2|File waktu modifikasi terakhir
|14|2|File tanggal modifikasi terakhir
|16|4|CRC-32
|20|4|Ukuran terkompresi
|24|4|Ukuran tidak terkompresi
|28|2|Panjang nama berkas (n)
|30|2|Panjang bidang ekstra (m)
|32|2|Panjang komentar berkas (k)
|34|2|Nomor disk tempat file dimulai
|36|2|Atribut file internal
|38|4|Atribut file eksternal
|42|4|Offset relatif dari header file lokal. Ini adalah jumlah byte antara awal disk pertama tempat file muncul, dan awal header file lokal. Ini memungkinkan perangkat lunak membaca direktori pusat untuk menemukan posisi file di dalam file ZIP.
|46|n|Nama berkas
|46+n|m|Bidang tambahan
|46+n+m|k|Ajukan komentar

#### Akhir Catatan Direktori Pusat


|Offset|Bytes|Deskripsi
---|---|---|
|0|4|Akhir tanda tangan direktori pusat # 0x06054b50
|4|2|Jumlah disk ini
|6|2|Disk tempat direktori pusat dimulai
|8|2|Jumlah catatan direktori pusat pada disk ini
|10|2|Jumlah total catatan direktori pusat
|12|4|Ukuran direktori pusat (byte)
|16|4|Offset dari awal direktori pusat, relatif terhadap awal arsip
|20|2|Panjang komentar (n)
|22|n|Komentar

## Referensi

* [Spesifikasi Format File ZIP PKWARE](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Struktur File PKZip](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)
