{
  "date" : "2019-12-16",
  "keywords" :[ "XLS", "file", "ekstensi", "format file", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Panduan format file Anda untuk mengetahui apa itu file XLS dan API yang dapat membuat dan membukanya.",
  "title" :"Apa itu format file XLS? Belajar dari Pakar Format File!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## Apa itu file XLS?

File dengan ekstensi XLS mewakili Format File Biner Excel. File tersebut dapat dibuat oleh Microsoft Excel serta program spreadsheet serupa lainnya seperti OpenOffice Calc atau Apple Numbers. File yang disimpan oleh Excel dikenal sebagai Buku Kerja dimana setiap buku kerja dapat memiliki satu atau lebih lembar kerja. Data disimpan dan ditampilkan kepada pengguna dalam format tabel di lembar kerja dan dapat mencakup nilai numerik, data teks, rumus, koneksi data eksternal, gambar, dan bagan. Aplikasi seperti Microsoft Excel memungkinkan Anda mengekspor data buku kerja ke beberapa format berbeda termasuk [PDF](/id/pdf/), [CSV](/id/spreadsheet/csv/), [XLSX](/id/spreadsheet/xlsx/), [TXT](/id/word-processing/txt/), [HTML](/id/web/html/), [XPS](/id/page-description-language/xps/), dan beberapa lainnya. Format file XLS diganti dengan format yang lebih terbuka dan terstruktur, XLSX, dengan rilis Microsoft Excel 2007. Versi terbaru masih memberikan dukungan untuk membuat dan membaca file XLS, meskipun XLSX adalah pilihan pertama yang digunakan sekarang.

## Sejarah Singkat

XLS dibuat oleh Microsoft untuk digunakan dengan Microsoft Excel dan juga dikenal sebagai Binary Interchange File Format (BIFF). Jenis file ini diperkenalkan pertama kali dengan menjadikannya bagian dari Excel untuk Windows pada tahun 1987. Spesifikasi format file XLS dipublikasikan pertama kali pada bulan Juni 2008 sebagai Revisi 1. Setelah itu, spesifikasi terus diperbarui dan tersedia revisi terbaru. per Agustus 2018 yang ditandai sebagai Revisi 8.0. Sejarah singkat berbagai versi format file XLS adalah sebagai berikut:

* Versi 7.0 (dirilis dengan office 95): Versi excel ini adalah yang paling kuat dan lebih cepat di antara semua versi dan penulisan ulang aliran internal diperbarui menjadi 32 bit.
* Versi 8 (dirilis dengan office 97): VBA diperkenalkan sebagai bahasa standar dan label bahasa alami yang dihapus digabungkan dalam versi ini untuk pertama kalinya. Itu juga memperkenalkan asisten kantor klip kertas untuk pertama kalinya.
* Versi 9 (Dirilis dengan office 2000): Hanya ada sedikit perubahan pada Versi 9 di mana asisten kantor klip kertas dapat memegang beberapa objek secara bersamaan yang sebelumnya tidak mungkin.
* Versi 10 (Dirilis dengan office XP): Versi ini tidak berisi peningkatan yang nyata.
* Versi 11 (Dirilis dengan office 2003): Pembaruan besar di versi 11, excel 2003 adalah pengenalan tabel baru.

## Spesifikasi Format File XLS ##

Data disusun dalam file XLS sebagai aliran biner dalam bentuk file gabungan seperti yang dijelaskan dalam [MS-CFB]. Data disimpan dalam file gabungan dengan menggunakan penyimpanan, aliran, dan sub aliran yang berisi informasi tentang konten dan struktur buku kerja, termasuk data buku kerja seperti definisi lembar kerja. Setiap aliran atau sub aliran berisi serangkaian catatan biner. Setiap rekaman biner berisi nol atau beberapa bidang terstruktur yang berisi data buku kerja. Bagian ini memberikan ikhtisar singkat tentang Struktur File XLS, tetapi untuk spesifikasi format file mendetail, Anda harus membaca [Spesifikasi Formasi File XLS](https://msdn.microsoft.com/en-us/library/cc313154(v#office .12).aspx) dokumen oleh Microsoft.

#### Aliran dan Subaliran ####

Buku kerja diwakili oleh aliran buku kerja. Setiap lembar kerja dalam buku kerja diwakili oleh Substream. Selain itu, ia memiliki Substream Lembar Bagan, Substream Lembar Makro, atau Substream Lembar Dialog yang mengikuti Substream Global. Setiap aliran atau sub aliran biner yang berisi data buku kerja HARUS ditulis sebagai rangkaian rekaman biner.

#### Catatan ####

Informasi tentang fitur dalam buku kerja disimpan sebagai rekaman yang merupakan urutan byte dengan panjang variabel. Catatan biner terdiri dari tiga komponen berikut:

**Jenis Rekam:** Jenis rekod adalah bilangan bulat tak bertanda dua byte yang menentukan jenis informasi apa yang ditentukan oleh rekod dan bagaimana struktur data rekod khusus untuk rekod ini diurutkan dan disusun. Nilai jenis rekaman HARUS berupa nilai dari Pencacahan Catatan (bagian 2.3) atau catatan HARUS memanfaatkan arsitektur rekaman yang akan datang (bagian 2.1.6).

**Ukuran Rekaman**: Ukuran rekaman adalah bilangan bulat tak bertanda dua byte yang menentukan jumlah byte yang menentukan ukuran total data rekaman. Ukuran rekaman HARUS lebih besar dari atau sama dengan 0 dan HARUS kurang dari atau sama dengan 8224.

**Data Rekam:** Komponen data rekod berisi bidang yang sesuai dengan jenis rekod tertentu dan terdiri dari sisa rekod. Urutan dan struktur bidang untuk jenis rekaman tertentu ditentukan di bagian terkait untuk jenis rekaman tersebut. Ukuran komponen data record HARUS sama dengan ukuran record. Bidang dalam komponen data rekaman dapat berisi nilai sederhana, larik nilai, struktur beberapa bidang, larik bidang, dan larik struktur.

#### Tabel Sel ####

Sel adalah blok dasar buku kerja yang menyimpan konten buku kerja seperti teks, rumus, dan data numerik. Sel mempertahankan catatan data yang disimpan melalui struktur data yang disebut Tabel Sel. Tabel Sel itu sendiri disimpan dalam urutan catatan yang sesuai dengan aturan CELLTABLE yang ditentukan dalam dokumen spesifikasi. Ini terdiri dari serangkaian blok baris di mana baris disusun dalam blok baris. Setiap blok baris berisi baris dari baris pertama yang berisi data hingga baris terakhir yang berisi data.

Pemformatan data atau baris disimpan dalam catatan Baris untuk setiap blok baris. Setiap sel yang berisi data atau pemformatan sel individual diwakili oleh catatan. Pemformatan yang terkait dengan sel dapat diturunkan dari pemformatan sel individual, pemformatan baris, pemformatan kolom, atau format sel default. Urutan prioritas untuk pemformatan adalah pemformatan sel individual dengan prioritas tertinggi, diikuti dengan pemformatan baris, lalu pemformatan kolom, lalu format sel default. Sel yang tidak berisi data dan tidak berisi pemformatan individual tidak akan disimpan.

#### Rumus ####

Rumus adalah urutan nilai, referensi sel, nama, fungsi, atau operator dalam sel yang bersama-sama menghasilkan nilai baru. Rumus disimpan dalam representasi tokenized yang dikenal sebagai "ekspresi yang diuraikan." Ekspresi yang diurai diubah menjadi formula tekstual pada waktu proses untuk tampilan dan pengeditan pengguna. Formula sel ditentukan oleh rekaman Formula. Rumus array ditentukan oleh catatan Array. Rumus bersama ditentukan oleh catatan ShrFmla.

#### Bagan ####

Lembar bagan menentukan bagan, grafik yang menampilkan data atau hubungan antara kumpulan data dalam bentuk visual, dan cache data bagan, salinan lokal dari data yang digunakan dalam data bagan hilang atau jika ditautkan ke eksternal sumber data rusak. Bagan menentukan grup satu atau dua sumbu, kumpulan sumbu yang diplotkan data bagan, dan kumpulan seri, garis tren, dan bilah kesalahan yang ditentukan dalam bagan. Setiap grup sumbu menentukan satu hingga empat grup bagan yang menentukan jenis visualisasi yang digunakan untuk menampilkan data. Setiap rangkaian, garis tren, dan bilah kesalahan menentukan grup bagan yang terkait dengannya.

#### Metadata ####

Metadata adalah data tambahan yang terkait dengan sel tertentu atau kontennya. Metadata direkam dalam BIFF8 hanya untuk tujuan ekstensibilitas di masa mendatang.

#### Tabel pivot ####

PivotTable adalah mekanisme untuk meringkas data sumber untuk mendapatkan gambaran umum tentang distribusi data tersebut. Dalam PivotTable, kolom yang berlaku dari data sumber menjadi bidang yang bisa digunakan untuk meringkas data. Saat data sumber PivotTable adalah data sumber OLAP, hierarki OLAP dan beberapa entitas OLAP lainnya menjadi bidang di PivotTable.
PivotTable memiliki dua bagian utama, tampilan PivotCache dan PivotTable. Mungkin ada beberapa tampilan PivotTable berdasarkan satu PivotCache non-OLAP.

#### Gaya ####

Gambaran umum ini menjelaskan bagaimana informasi pemformatan dan perlindungan untuk sel dalam lembar (1) ditentukan. Pemformatan sel terdiri dari beberapa set properti:

* Properti font (tebal, miring, warna font, ukuran font, dll…)
* Isi properti (warna latar depan, warna latar belakang, pola, gradien, dll…)
* Properti perataan (kiri, tengah, perataan kanan, dll…)
* Properti batas (kiri, kanan, atas, bawah, tebal atau tipis, warna, dll…)
* Properti pemformatan angka (tanggal, waktu, jumlah tempat desimal, dll…)
* Properti perlindungan (terkunci, tersembunyi, dll...)

Properti ini, secara keseluruhan, menjelaskan bagaimana sel tertentu ditampilkan dan dicetak.

## Referensi ##

* [[MS-XLS] - Struktur Format File Biner Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] - Format File Biner File Gabungan](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

