{
  "date" : "2019-10-11",
  "keywords" :[ "file gz", "format file gz", "apa itu file gz", "file", "contoh gz", "ekstensi file gz", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File GZ - File Arsip Zip GNU",
  "description":"Pelajari tentang apa itu file GZ dan API yang dapat membuat dan membuka file GZ.",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file GZ?

File GZ adalah arsip terkompresi yang dibuat menggunakan algoritme kompresi [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) standar. Itu mungkin berisi beberapa file terkompresi, direktori dan potongan file. Format ini awalnya dikembangkan untuk menggantikan format kompresi pada sistem UNIX. dan masih menjadi salah satu jenis arsip paling umum di sistem Linux. Aplikasi seperti [WinZip](https://www.winzip.com/en/) dapat membuka file GZ untuk melihat kontennya di Windows dan MacOS.

## Format File GZ - Informasi Lebih Lanjut

Gzip menggunakan algoritme [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) untuk kompresi arsip dan berbeda dari format arsip [ZIP](/id/compression/zip/) dalam menerapkan algoritme kompresi pada arsip lengkap daripada file individual. Spesifikasi format file GZIP versi 4.3 yang diterbitkan oleh Internet Engineering Task Force (IETF) berisi informasi mendetail tentang format file. Format filenya terdiri dari:

* Judul File
* Header Opsional
* Data Terkompresi
* File Footer

## Tajuk Berkas GZ ##

Header file GZ terdiri dari 10 byte sebagai berikut:

|Offset|Ukuran|Nilai|Deskripsi
---|---|---|---|
|0|2|0x1f 0x8b|Nomor ajaib yang mengidentifikasi jenis file
|2|1| |Metode Kompresi * 0-7 (Dicadangkan) * 8 (Mengempis)
|3|1| | File Bendera
|4|4| |Stempel waktu 32-bit
|8|1| | Bendera kompresi
|9|1| | ID sistem operasi

### Bendera Berkas ###

|Nilai|Identifier|Deskripsi
---|---|---|
|0x01|FTEXT|Jika disetel, data yang tidak terkompresi perlu diperlakukan sebagai teks, bukan data biner. Tanda ini mengisyaratkan konversi akhir baris untuk file teks lintas platform tetapi tidak menerapkannya.
|0x02|FHCRC|Berkas berisi header checksum (CRC-16)
|0x04|FEXTRA|Berkas berisi bidang tambahan
|0x08|FNAME|Berkas berisi string nama berkas asli
|0x10|FCOMMENT|Berkas berisi komentar
|0x20| |Dicadangkan
|0x40| |Dicadangkan
|0x80| |Dicadangkan

### Sistem operasi ###

|Nilai|Deskripsi
---|---|
|0|Sistem berkas FAT (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (atau OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari TOS
|6|Sistem berkas HPFS (OS/2, NT)
|7|Macintosh
|8|Sistem-Z
|9|CP/M
|10|TOPS-20
|11|Sistem berkas NTFS (NT)
|12|QDOS
|13|Acorn RISCOS
|255|tidak diketahui

## Header Opsional GZ ##

Header tambahan opsional adalah yang dilambangkan dengan flag file dan menyertakan informasi seperti nama file asli, kolom tambahan, komentar, dan checksum header.

## Data Terkompresi ##

Bagian ini berisi data terkompresi menggunakan algoritma kompresi DEFLATE.

## Footer Berkas GZ ##

Footer file berukuran 8 byte dan berisi informasi berikut.

|Offset|Ukuran|Deskripsi
---|---|---|
|0|4|Checksum (CRC-32)
|4|4|Nilai ukuran data tidak terkompresi dalam byte

## Referensi ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: spesifikasi format file GZIP](https://datatracker.ietf.org/doc/html/rfc1952), oleh IETF.

