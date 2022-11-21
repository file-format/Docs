{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SATU - Format File Microsoft OneNote",
  "description":"Pelajari tentang SATU format file dan API yang dapat membuat dan membuka SATU file.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file .ONE? ##

File yang diwakili oleh ekstensi .ONE dibuat oleh aplikasi Microsoft OneNote. OneNote memungkinkan Anda mengumpulkan informasi menggunakan aplikasi seolah-olah Anda menggunakan buku draf untuk membuat catatan. File OneNote bisa berisi elemen berbeda yang bisa ditempatkan di lokasi tidak tetap di halaman dokumen. Elemen ini dapat berisi teks, tulisan tangan digital, dan objek yang disalin dari aplikasi lain termasuk gambar, lukisan, dan klip multimedia (audio/video). Microsoft kini menawarkan versi online OneNote sebagai bagian dari Office365 di mana Notes dapat dibagikan dengan pengguna OneNote lain melalui internet.

## Spesifikasi Format File .ONE ##

Format file OneNote menyediakan cara yang efektif untuk merepresentasikan catatan digital sebagai rangkaian hierarki bagian dan halaman. Setiap halaman berisi konten yang ditentukan pengguna dalam struktur khusus untuk representasi dengan format file Document Object Model (DOM). Model data untuk format ini seperti yang diilustrasikan di bawah ini.

### Ikhtisar Struktur ###

Seperti yang diilustrasikan dalam model data untuk format file OneNote, dokumen OneNote terdiri dari berbagai elemen.

#### Bagian ####

Bagian adalah wadah paling atas dalam file OneNote yang selanjutnya berisi berbagai elemen di dalamnya seperti:

* Halaman
* Metadata
* Properti

Metadata dan properti menyertakan nama bagian, identifikasi halaman yang terdapat di bagian, dan urutan munculnya halaman tersebut. Istilah "bagian" mengacu pada semua halaman yang ada di bagian dan representasi data tersebut dalam file penyimpanan revisi OneNote®, yang memiliki ekstensi nama file .one.

#### Halaman ####

Konten yang ditentukan pengguna dalam dokumen OneNote terdapat di dalam halaman. Informasi halaman mencakup teks, daftar, tabel, judul halaman, gambar, dan tag catatan. Sebuah halaman terdiri dari objek kerangka yang sebagian besar objek yang terkandung ditambahkan. Setiap halaman dapat diberi nama untuk representasi yang bermakna dan objek dapat ditambahkan langsung ke halaman juga. Sebuah halaman selanjutnya dapat berisi sub-halaman dalam sistem hierarkis.

#### Properti dan Kumpulan Properti ####

Konten OneNote terdiri dari properti, kumpulan properti, dan objek data file. Kumpulan properti adalah kumpulan properti yang mewakili beberapa jenis konten. Objek data file adalah blok data biner yang berisi gambar, file tersemat, atau konten audio/video.

#### Buku Catatan OneNote ####

Buku catatan adalah kumpulan file bagian yang disimpan di direktori yang sama. Kumpulan properti digunakan untuk menentukan pengaturan seperti urutan bagian dalam buku catatan dan warna buku catatan.

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

|Format Berkas|Nilai
--- | --- |
|.satu|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Unsigned integer. HARUS menjadi salah satu nilai dalam tabel berikut, bergantung pada format file dari file ini.

|Format Berkas|Nilai
--- | --- |
|.satu|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 byte):` Struktur **FileChunkReference32** yang HARUS memiliki nilai "fcrZero".

`fcrLegacyTransactionLog (8 byte):` Struktur **FileChunkReference32** yang HARUS berupa "fcrNil".

`cTransactionsInLog (4 byte):` Bilangan bulat tak bertanda yang menentukan jumlah transaksi dalam log transaksi. TIDAK HARUS nol.

`cbLegacyExpectedFileLength (4 bytes):` Unsigned integer yang HARUS nol, dan HARUS diabaikan.

`rgbPlaceholder (8 bytes):` Unsigned integer yang HARUS nol, dan HARUS diabaikan.

`fcrLegacyFileNodeListRoot (8 byte):` Struktur **FileChunkReference32** yang HARUS berupa "fcrNil".

`cbLegacyFreeSpaceInFreeChunkList (4 byte):` Bilangan bulat tak bertanda yang HARUS nol, dan HARUS diabaikan.

`fNeedsDefrag (1 byte):` HARUS diabaikan.

`fRepairedFile (1 byte):` HARUS diabaikan.

`fNeedsGarbageCollect (1 byte):` HARUS diabaikan.

`fHasNoEmbeddedFileObjects (1 byte):` Unsigned integer yang HARUS nol, dan HARUS diabaikan.

`guidAncestor (16 bytes):` GUID yang menentukan bidang **Header.guidFile** dari file daftar isi, diberikan oleh tabel berikut:


|Format File Daftar Isi|Lokasi File Daftar Isi
--- | --- |
|Berkas Bagian - .Satu|Berkas daftar isi terletak di direktori yang sama dengan berkas ini.
|File Daftar Isi - .onetoc2|File daftar isi terletak di direktori induk file ini.

Jika GUID adalah {00000000-0000-0000-0000-000000000000}, bidang ini tidak mereferensikan file daftar isi.

`crcName (4 bytes):` Unsigned integer yang menentukan nilai CRC dari nama file penyimpanan revisi ini. Nama adalah representasi Unicode dari nama file dengan ekstensinya dan karakter nol tambahan di bagian akhir. CRC ini selalu dihitung menggunakan algoritma CRC untuk file .one, terlepas dari format file penyimpanan revisi ini.

`fcrHashedChunkList (12 byte):` Struktur **FileChunkReference64x32** yang menentukan referensi ke **FileNodeListFragment** pertama dalam daftar potongan yang di-hash. Jika nilai struktur **FileChunkReference64x32** adalah "fcrZero" atau "fcrNil", daftar potongan hash tidak ada.

`fcrTransactionLog (12 bytes):` Struktur **FileChunkReference64x32** yang menentukan referensi ke struktur **TransactionLogFragment** pertama dalam log transaksi. Nilai kolom **fcrTransactionLog** TIDAK HARUS "fcrZero" dan TIDAK HARUS "fcrNil".

`fcrFileNodeListRoot (12 byte):` Struktur **FileChunkReference64x32** yang menentukan referensi ke daftar node file root. Nilai kolom **fcrFileNodeListRoot** TIDAK HARUS "fcrZero" dan TIDAK HARUS "fcrNil".

`fcrFreeChunkList (12 bytes):` Struktur **FileChunkReference64x32** yang menentukan referensi ke struktur **FreeChunkListFragment** pertama. Jika nilai struktur **FileChunkReference64x32** adalah "fcrZero" atau "fcrNil", daftar potongan gratis tidak ada.

`cbExpectedFileLength (8 bytes):` Unsigned integer yang menentukan ukuran, dalam byte, dari file penyimpanan revisi ini.

`cbFreeSpaceInFreeChunkList (8 bytes):` Unsigned integer yang HARUS menentukan ukuran, dalam byte, ruang kosong yang ditentukan oleh daftar potongan bebas.

`guidFileVersion (16 byte):` GUID. Saat nilai bidang **cTransactionsInLog** atau bidang **guidDenyReadFileVersion** diubah, **guidFileVersion** HARUS diubah ke GUID baru.

`nFileVersionGeneration (8 bytes):` Unsigned integer yang menentukan berapa kali file telah berubah. HARUS bertambah bila kolom **guidFileVersion** berubah.

`guidDenyReadFileVersion (16 byte):` GUID. Saat konten file yang ada diubah, tidak termasuk struktur **Header** file dan blok penyimpanan yang tidak digunakan, **guidDenyReadFileVersion** HARUS diubah menjadi GUID baru.

`grfDebugLogFlags (4 byte):` HARUS nol. HARUS diabaikan.

`fcrDebugLog (12 byte):` Struktur **FileChunkReference64x32** yang HARUS memiliki nilai "fcrZero". HARUS diabaikan.

`fcrAllocVerificationFreeChunkList (12 byte):` Struktur **FileChunkReference64x32** yang HARUS berupa "fcrZero". HARUS diabaikan.

`bnCreated (4 bytes):` Unsigned integer yang menentukan nomor build aplikasi yang membuat file penyimpanan revisi ini. HARUS diabaikan.

`bnLastWroteToThisFile (4 bytes):` Unsigned integer yang menentukan nomor build aplikasi yang terakhir menulis ke file penyimpanan revisi ini. HARUS diabaikan.

`bnOldestWritten (4 bytes):` Unsigned integer yang menentukan nomor build dari aplikasi terlama yang menulis ke file penyimpanan revisi ini. HARUS diabaikan.

`bnNewestWritten (4 bytes):` Unsigned integer yang menentukan nomor build dari aplikasi terbaru yang menulis ke file penyimpanan revisi ini. HARUS diabaikan.

`rgbReserved (728 byte):` HARUS nol. HARUS diabaikan.

## Referensi ##

* [[MS-ONESTORE] - Format File OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

