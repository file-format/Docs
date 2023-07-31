{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File PDF - File Database Program",
  "description":"Pelajari tentang format file PDB dan API yang dapat membuat dan membuka file PDB.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Apa itu file PDB?

File dengan ekstensi .pdb adalah file database program yang berisi informasi debug untuk file executable yang dikompilasi (EXE/DLL). File PDB dihasilkan oleh Microsoft Compilers saat program aplikasi dikompilasi dalam mode debug. Kehadiran file PDB dapat membantu merekayasa balik sebuah file yang dapat dieksekusi karena berisi informasi penting tentang semua simbol modul. Karena alasan inilah file-file ini dipisahkan dari file yang dapat dieksekusi terakhir. [DgbHelp API] Microsoft (https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) dapat membuka file PDB untuk mendapatkan informasi seperti publik dan ekspor, simbol global, simbol lokal, ketik data, file sumber, dan nomor baris.

## Format File PDB

PDB adalah format file milik Microsoft dan belum didokumentasikan secara resmi di mana pun. Namun, dokumentasi awal tersedia [di sini](https://github.com/Microsoft/microsoft-pdb) dan dapat dirujuk.

### Aliran PDB

File PDB terdiri dari beberapa aliran di mana setiap aliran bertindak sebagai file individu virtual dan berisi informasi. Penulis file PDB dapat menulis ke file-file ini dan file diselesaikan hanya setelah komit eksplisit dikeluarkan. Kompiler dapat terus menulis ke file PDB tetapi melakukan hanya jika semua kode pengguna berhasil dikompilasi. File PDB terdiri dari aliran berikut:

|Nomor Streaming |Isi |Deskripsi Singkat|
---|---|---|
|1| Pdb (header) |Informasi versi, dan informasi untuk menghubungkan PDB ini ke EXE|
|2| Tpi (Pengelola tipe) |Semua tipe yang digunakan dapat dieksekusi.|
|3| Dbi (Informasi debug) |Menyimpan kontribusi bagian, dan daftar 'Mods'|
|4| Peta Nama| Memegang tabel string hash|
|4-(n+4)| n Mod (Informasi modul)| Setiap aliran Mod memegang simbol dan nomor baris untuk satu kompilasi |
|n+4| hash simbol global| Indeks yang memungkinkan pencarian dalam simbol global berdasarkan nama|
|n+5| hash simbol publik| Indeks yang memungkinkan pencarian dalam simbol publik berdasarkan alamat|
|n+6| Catatan simbol | Rekaman simbol aktual dari simbol global dan publik|
|n+7| Ketik hash| Hash digunakan oleh aliran TPI.|

Setiap aliran dalam file PDB terdiri dari beberapa halaman yang tidak harus diberi nomor secara berurutan.

### judul PDB

File PDB dengan Header yang terdiri dari tanda tangan untuk mengidentifikasi dan memvalidasi format tertentu. Panjang tanda tangan tergantung pada format PDB. Header mungkin lebih panjang dari satu halaman.

### Metadata PDB
Metadata PDB bertanggung jawab untuk mengenali semua aliran komponen, memberikan panjang, dan urutan halaman untuk setiap aliran. Perintah diberikan ke streaming secara berurutan; dimulai dengan 0. Ada juga aliran akar yang tidak terurut, yang berisi beberapa metadata.

## Referensi
* [PDB - Wikipedia](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

