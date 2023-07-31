{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "file", "ekstensi", "format file", "Word", "Dokumen" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - File Dokumen Microsoft Word",
  "description":"Pelajari tentang format file DOC dan API yang dapat membuat dan membuka file DOC.",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Apa itu file DOC?

File dengan ekstensi .doc mewakili dokumen yang dihasilkan oleh Microsoft Word atau dokumen pengolah kata lainnya dalam format file biner. Ekstensi awalnya digunakan untuk dokumentasi teks biasa pada beberapa sistem operasi yang berbeda. Itu dapat berisi beberapa jenis data yang berbeda seperti gambar, diformat serta teks biasa, grafik, bagan, objek yang disematkan, tautan, halaman, pemformatan halaman, pengaturan cetak dan banyak lainnya. Formatnya populer untuk semua jenis dokumentasi karena beragam opsi yang ditawarkannya kepada pengguna untuk menulis manual, proposal, spesifikasi, resume, artikel, atau dokumen serupa lainnya. Versi terbaru DOC adalah [DOCX](/id/word-processing/docx/) yang didasarkan pada Office OpenXML yang spesifikasinya tersedia secara terbuka.

## Sejarah Singkat ##

WordPerfect, sebuah produk dari [Corel](https://www.corel.com/en/), menggunakan DOC sebagai perpanjangan dari format kepemilikan mereka. Pada 1980-an, WordPerfect tetap menjadi pilihan penggunaan di sebagian besar komputer karena ketersediaannya yang mudah, sesuai dengan sebagian besar mesin komputer dan sistem Operasi. Namun, WordPerfect melihat kejatuhannya pada OS Windows ketika Microsoft memperkenalkan Microsoft Word sebagai produknya untuk format file dokumen dan memilih ekstensi DOC untuk format hak milik mereka. Ketika Microsoft Word menjadi semakin populer, format file DOC mengalami beberapa revisi dari Microsoft Word 97 - 2003. Itu adalah tahun 2007 ketika format file DOC default digantikan oleh format Office Open XML (dikenal sebagai DOCX) dan versi baru dari Microsoft Word sekarang menggunakan ekstensi baru ini sebagai format file default.

## Spesifikasi Format File DOC - Informasi Lebih Lanjut

Microsoft tidak merilis spesifikasi format file DOC untuk waktu yang lama hingga 2008. Pada Februari 2008, spesifikasi format dirilis untuk format file .doc di bawah Janji Spesifikasi Terbuka Microsoft. Meskipun spesifikasinya tidak menjelaskan semua fitur yang digunakan oleh format DOC, spesifikasi ini memberikan banyak informasi tentang pengetahuan yang dibutuhkan untuk bekerja dengan format file ini. Namun, rekayasa balik diperlukan untuk memanfaatkan informasi yang tersedia. Spesifikasi telah diperbarui beberapa kali dan [revisi](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) terbaru adalah 8.0 yang diperbarui per Agustus 2018 .

### Beberapa Konsep Dasar ###

Sebelum kita membahas detail tentang spesifikasi format file untuk DOC, beberapa konsep dasar perlu dipahami agar dapat bekerja dengan format file ini.

**File Information Base (Fib):** Struktur Fib berisi informasi tentang dokumen dan menentukan pointer file ke berbagai bagian yang menyusun dokumen.
Fib adalah struktur panjang variabel. Dengan pengecualian bagian dasar yang ukurannya tetap, setiap bagian didahului dengan bidang hitungan yang menentukan ukuran bagian berikutnya.

**Posisi Karakter:** CP atau Posisi Karakter mewakili bilangan bulat 32-bit tak bertanda tangan yang berfungsi sebagai indeks karakter berbasis nol dalam teks dokumen. Lokasi dan ukuran setiap karakter dalam file tidak dapat diambil secara langsung dan harus dihitung menggunakan algoritme yang ditentukan sebelumnya. Karakter meliputi:

* Teks dokumen
* Jangkar objek seperti catatan kaki atau kotak teks
* Kontrol karakter seperti tanda paragraf dan tanda sel tabel

**PLC:** Struktur PLC adalah larik CP yang diikuti larik elemen data. Elemen data untuk setiap PLC harus berukuran sama dengan nol atau lebih byte, dan untuk alasan ini, jumlah CP harus lebih dari jumlah elemen data. Struktur PLC memiliki jenis yang berbeda di mana setiap jenis menentukan apakah duplikat CP diperbolehkan untuk jenis itu atau tidak. Struktur PLC terdiri dari:

* **aCP (panjang variabel):** Larik elemen CP. Setiap jenis struktur **PLC** menentukan arti elemen CP dan rentang yang diizinkan.
* **aData (panjang variabel):** Setiap jenis struktur **PLC** menentukan struktur dan makna elemen data, batasan apa pun pada jumlah elemen data, dan batasan apa pun pada data yang terkandung di dalamnya. Itu juga menentukan hubungan antara elemen data dan CP yang sesuai.

**Pilihan Valid:** Konstruksi file .DOC sebagian besar dijelaskan oleh berbagai CP. Ada sejumlah [aturan](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) yang ditentukan oleh Microsoft untuk diikuti dalam kasus tersebut.

**STTB:** STTB adalah tabel string yang terdiri dari header yang diikuti oleh larik elemen. Nilai **cData** menentukan jumlah elemen yang terdapat dalam larik.

**Penyimpanan Properti:** File kata mungkin memiliki elemen yang berbeda seperti teks, paragraf, tabel, gambar, dan bagian yang masing-masing dapat memiliki propertinya sendiri. Properti ini disimpan dalam file Word sebagai perbedaan dari default. Perbedaan tersebut ditentukan oleh PRl yang terdiri dari Single Property Modifier (Sprm) dan operannya. Aplikasi dapat menentukan kumpulan properti terakhir dengan menerapkan daftar **Prl**s.

**Perlindungan Kata Sandi:** File Word juga dapat dilindungi kata sandi, dengan salah satu mekanisme berikut dapat digunakan.

* Kebingungan XOR
* Enkripsi dokumen biner Office RC4
* Enkripsi dokumen biner Office RC4 CryptoAPI

Jika FibBase.fEncrypted dan FibBase.fObfuscation sama-sama 1, file dikaburkan dengan menggunakan pengaburan XOR.

Jika FibBase.fEncrypted adalah 1 dan FibBase.fObfuscation adalah 0, file dienkripsi dengan menggunakan Enkripsi Office Binary Document RC4 atau Office Binary Document RC4 CryptoAPI Encryption, dengan EncryptionHeader disimpan dalam byte FibBase.lKey pertama dari aliran Tabel. EncryptionHeader.EncryptionVersionInfo menentukan mekanisme enkripsi mana yang digunakan untuk mengenkripsi file.

### Struktur Berkas ###

File Word biner dalam orisinalitasnya adalah file gabungan OLE yang terdiri dari beberapa penyimpanan dan aliran. Penyimpanan dan aliran ini memiliki struktur dan ukurannya sendiri, yang menentukan parameter untuk menulis dan membaca. Ini adalah:

#### Aliran Dokumen Word ####

Aliran ini berisi teks dokumen dan informasi lain yang direferensikan dari bagian lain file. Aliran tidak memiliki struktur yang ditentukan sebelumnya selain FIB di awal yang wajib dan harus diimbangi 0. Aliran ini tidak boleh lebih besar dari 2147 MB.

#### 1TableStream atau 0TableStream ####

File Word biner dapat berisi Aliran Tabel yang dikenal sebagai aliran 1Tabel atau aliran 0Tabel. Setidaknya satu dari ini harus ada dalam dokumen. Namun, jika dokumen berisi aliran 1Table dan 0Table, hanya aliran yang direferensikan oleh base.fWhichTblStm yang digunakan. Aliran yang tidak direferensikan HARUS diabaikan.
Aliran Tabel TIDAK HARUS lebih besar dari 2147 MB.

#### Aliran data ####

Aliran data tidak memiliki struktur yang ditentukan sebelumnya. Ini berisi data yang direferensikan dari FIB atau dari bagian lain dari file. Aliran ini tidak perlu ada jika tidak ada referensi untuk itu. Aliran Data TIDAK HARUS lebih besar dari 2147 MB.

#### Penyimpanan Kumpulan Objek ####

Penyimpanan Object Pool berisi penyimpanan untuk objek OLE tertanam. Penyimpanan ini tidak perlu ada jika tidak ada objek OLE yang disematkan dalam dokumen.

#### Penyimpanan Data XML Khusus ####

Penyimpanan Data Custom XML adalah penyimpanan opsional yang namanya HARUS "MsoDataStore".

#### Aliran Informasi Rangkuman ####

Aliran Informasi Ringkasan adalah aliran opsional yang namanya HARUS "\005SummaryInformation", di mana \005 adalah karakter dengan nilai 0x0005, dan bukan string literal "\005".

#### Aliran Informasi Ringkasan Dokumen ####

Aliran Informasi Ringkasan Dokumen adalah aliran opsional yang namanya HARUS "\005DocumentSummaryInformation", dengan \005 adalah karakter dengan nilai 0x0005, bukan string literal "\005".

#### Aliran Enkripsi ####

Aliran Enkripsi adalah aliran opsional yang namanya HARUS "enkripsi". Aliran ini TIDAK HARUS ada kecuali kedua kondisi berikut terpenuhi:

* Dokumen dienkripsi dengan Office Binary Document RC4 CryptoAPI Encryption.
* Nilai fDocProps diatur di EncryptionHeader.Flags.

#### Penyimpanan Makro ####

Penyimpanan Makro adalah penyimpanan opsional yang berisi makro untuk file. Jika ada, itu HARUS merupakan Project Root Storage.

#### Penyimpanan Tanda Tangan XML ####

Penyimpanan tanda tangan XML adalah penyimpanan opsional yang namanya HARUS "_xmlsignatures".

#### Aliran Tanda Tangan ####

Aliran tanda tangan adalah aliran opsional yang namanya HARUS "_signatures". Aliran ini berisi tanda tangan digital.

#### Penyimpanan Ruang Data Manajemen Hak Informasi ####

Penyimpanan Ruang Data Manajemen Hak Informasi adalah penyimpanan opsional yang namanya HARUS "\006DataSpaces", di mana \006 adalah karakter dengan nilai 0x0006, dan bukan string literal "\006". Jika penyimpanan ini ada, Aliran Konten yang Dilindungi juga HARUS ada.
Jika ada penyimpanan ini, semua aliran dan penyimpanan yang ditentukan selain penyimpanan ini dan Aliran Konten yang Dilindungi HARUS dibaca dari Aliran Konten yang Dilindungi sebagaimana ditentukan dalam [MS-OFFCRYPTO] dan jika ada aliran dan penyimpanan tersebut ada di luar Konten yang Dilindungi Stream, mereka HARUS diabaikan.

#### Aliran Konten yang Dilindungi ####

Aliran Konten Terproteksi adalah aliran opsional yang namanya HARUS "\009DRMContent", dengan \009 adalah karakter dengan nilai 0x0009, dan bukan string literal "\009".
Jika aliran ini ada, Penyimpanan Ruang Data Manajemen Hak Informasi HARUS juga ada.

## Referensi ##

* [Spesifikasi Formasi File MS-DOC](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Komputasi Doc](https://en.wikipedia.org/wiki/Doc_(komputasi))

