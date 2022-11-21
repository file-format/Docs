{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Format File Microsoft OneNote",
  "description":"Pelajari tentang format file ONETOC2 dan API yang dapat membuat dan membuka file ONETOC2.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu ONETOC2? ##

Mereka yang telah bekerja dengan aplikasi [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) mungkin telah memperhatikan keberadaan file .onetoc2 di folder notebook. Microsoft OneNote membuat file biner .onetoc2 sebagai Daftar Isi untuk menyimpan indeks tentang pengurutan berbagai bagian pembuatan catatan di buku catatan. Buku catatan adalah kumpulan file bagian yang disimpan di direktori yang sama. File .onetoc2 menggunakan kumpulan properti untuk menentukan pengaturan seperti urutan bagian dalam buku catatan dan warna buku catatan.

Saat Anda membuat buku catatan di OneNote 2016, buku catatan disimpan secara otomatis dalam format file 2010-2016 yang baru. Anda memerlukan format ini jika ingin semua fitur di OneNote 2016, seperti persamaan matematika dan catatan tertaut, berfungsi dengan benar.

## Format File ONETOC2 ##

Format file .onetoc2 direpresentasikan sebagai OneNote Revision Store File Format dan merupakan kumpulan struktur yang menentukan penyimpanan revisi yang diatur ke dalam ruang objek referensi silang, berisi objek dengan kumpulan properti, dan berisi log transaksi untuk memastikan integritas file di asinkron menulis. Spesifikasi lengkap untuk format file .onetoc2 tersedia [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) dan dapat dirujuk untuk pengembangan aplikasi .

### Struktur Berkas ###

File penyimpanan revisi HARUS dimulai dengan struktur **Header**. Sisa file dipartisi menjadi blok-blok byte, di mana ukuran dan struktur setiap blok ditentukan oleh bidang yang mereferensikannya. Blok dapat dijangkau jika direferensikan oleh struktur **Header**, atau jika direferensikan oleh bidang di blok lain yang dapat dijangkau. Data di luar struktur **Header** dan semua blok yang dapat dijangkau HARUS diabaikan.

Semua struktur disejajarkan pada batas 1-byte. Semua bilangan bulat ditandatangani kecuali ditentukan lain. Semua bidang adalah [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) kecuali ditentukan lain.

#### Tajuk ####

Header file .ONE terdiri dari potongan-potongan yang berisi id dan bidang unik yang berbeda untuk representasi informasi file sebagai berikut:

`guidFileType (16 bytes):` GUID yang menentukan jenis file penyimpanan revisi. HARUS menjadi salah satu nilai dari tabel berikut.

|Format Berkas|Nilai
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` GUID yang menentukan identitas file penyimpanan revisi ini. HARUS unik secara global.

`guidLegacyFileVersion (16 byte):` HARUS berupa "{00000000-0000-0000-0000-000000000000}" dan HARUS diabaikan.

`guidFileFormat (16 bytes):` GUID yang menentukan bahwa file tersebut adalah file penyimpanan revisi. HARUS "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

`ffvLastCodeThatWroteToThisFile (4 byte):` Unsigned integer. HARUS menjadi salah satu nilai dalam tabel berikut, bergantung pada jenis file.

|Format Berkas|Nilai
--- | --- |
|.satu|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 byte):` Sebuah unsigned integer. HARUS menjadi salah satu nilai dalam tabel berikut, bergantung pada format file dari file ini.


|Format Berkas|Nilai
--- | --- |
|.satu|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 byte):` Sebuah unsigned integer. HARUS menjadi salah satu nilai dalam tabel berikut, bergantung pada format file dari file ini.
:


|Format Berkas|Nilai
--- | --- |
|.satu|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Unsigned integer. HARUS menjadi salah satu nilai dalam tabel berikut, bergantung pada format file dari file ini.


|Format Berkas|Nilai
--- | --- |
|.satu|0x0000002A
|.onetoc2|0x0000001B

## Referensi ##

* [[MS-ONESTORE] - Format File OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

