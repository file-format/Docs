{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File EDB - File Database Exchange Mail",
  "description":"Pelajari tentang format file EDB dan API yang dapat membuat dan membuka file EDB.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## Apa itu file EDB?

File dengan ekstensi file .edb adalah database kotak surat yang dibuat oleh Microsoft Exchange Server untuk menyimpan data terkait email. EDB, Exchange Database, menyimpan pesan yang sedang dalam proses dan non-SMTP. EDB juga dikenal sebagai file Database Extensible Storage Engine (ESE) dan menyimpan file menggunakan struktur b-tree. Menjadi file penyimpanan, file EDB dapat diubah menjadi format file penyimpanan surat lain seperti [PST](/id/email/pst/) dan [OST](/id/email/ost/).

## Format File EDB

Tidak ada spesifikasi format file EDB resmi/terbuka yang tersedia yang dapat dirujuk. Beberapa kemajuan telah dibuat untuk merekayasa balik format file, menghasilkan decoding spesifikasi parsial. Sesuai ini, file EDB terdiri dari:
* File Header - Berisi informasi header file database
* Halaman Ukuran Tetap - Berisi database yang terdiri dari tabel dan indeks

### Kepala File Basis Data
Header file database berada di halaman database pertama dan berukuran minimal 668 byte. Header file berisi `File Format Version` dan `File Type` selain bidang lainnya.

#### Jenis File
|Tipe|Deskripsi
---|---|
|0| Basis data|
|1| Streaming|

`Catatan:` Pengidentifikasi untuk jenis ini tidak diketahui.

#### Versi Format File
Format asli EDB dimulai pada April 1997 dan terus berkembang untuk perubahan setelahnya.

|Tanggal Revisi|Versi|Revisi|deskripsi
---|---|---|---|
|Apr 1997| 0x00000620|0x00000000| Format Beta sistem operasi asli.|
|Mei 1997 |0x00000620|0x00000001| Tambahkan kolom dalam katalog untuk pengindeksan bersyarat dan OLD.|
|Jun 1997|0x00000620|0x00000002|Tambahkan flag fLocalizedText di IDB.|
|Oct 1997|0x00000620|0x00000003|Tambahkan SPLIT_BUFFER ke halaman root pohon ruang angkasa.|
|Jan 1998|0x00000620|0x00000002|Kembalikan revisi agar ESE97 tetap kompatibel ke depan.|
||0x00000620|0x00000003|Tambahkan kolom baru yang diberi tag ke katalog ("CallbackData" dan "CallbackDependencies").|
|Mei 1998|0x00000620|0x00000004|Super Long Value (SLV) support: signSLV, fSLVExists in dbheader.|
|Mei 1998|0x00000620|0x00000005|Pohon luar angkasa SLV baru.|
|Okt 1998|0x00000620|0x00000006|Peta luar angkasa SLV.|
|Des 1998|0x00000620|0x00000007|4-byte IDXSEG.|
|Jan 1999|0x00000620|0x00000008|Format kolom template baru.|
|Jun 1999|0x00000620|0x00000009|Kolom template yang diurutkan. Digunakan di Windows XP SP3|
||0x00000620|0x0000000b|Berisi header halaman dengan checksum ECCDigunakan di Exchange|
||0x00000620|0x0000000c|Digunakan di Windows Vista (SP0)|
||0x00000620|0x00000011|Dukungan untuk halaman 2 KiB, 16 KiB, dan 32 KiB. Header halaman yang diperluas dengan checksum ECC tambahan. Kompresi kolom. Petunjuk ruang. Digunakan di Windows 7 (SP0)|
|Mei 1999|0x00000623|0x00000000|Pengelola Ruang Baru.|

### File Basis Data

File basis data EDB berisi skema untuk semua tabel dalam basis data. Selain itu, ini juga menyertakan rekaman untuk semua tabel database dan indeks untuk tabel tersebut. Lokasinya ditentukan oleh pengidentifikasi berikut.

* JetCreateDatabase
* JetCreateDatabase2
* JetAttachDatabase
* JetAttachDatabase2

Berdasarkan ini, keadaan database dapat dinilai sebagai berikut.

|Nilai|Identifier|Deskripsi
---|---|---|
|1|JET_dbstateJustCreated|Basis data baru saja dibuat.|
|2|JET_dbstateDirtyShutdown|Database memerlukan pemulihan keras atau lunak untuk dijalankan agar dapat digunakan atau dipindahkan. Seseorang seharusnya tidak mencoba memindahkan database dalam keadaan ini.|
|3|JET_dbstateCleanShutdown|Basis data dalam keadaan bersih. Basis data dapat dilampirkan tanpa file log apa pun.|
|4|JET_dbstateBeingConvert|Database sedang ditingkatkan.|
|5|JET_dbstateForceDetachInternal|Nilai ini diperkenalkan di WindowsXP|
 

## Referensi
* [Spesifikasi Extensible Storage Engine (ESE) Database File (EDB)](https://github.com/libyal/libesedb/tree/master/documentation)

