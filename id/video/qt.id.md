{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File QT - File Film Cepat",
  "keywords" :[ "QT", "Video QuickTime", "format qt", "cara memutar file qt", "File Film Cepat", "QTFF", "video", "Apple" ],
  "description":"Pelajari tentang format file QT dan API yang dapat membuat dan membuka file QT.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Apa itu file QT?

File dengan ekstensi .qt adalah file wadah multimedia yang digunakan oleh kerangka kerja QuickTime untuk menyimpan konten file multimedia. Dikembangkan oleh Apple Inc. QuickTime File Format (QTFF) adalah file wadah multimedia yang berisi audio, video, atau teks untuk diputar nanti. Ini adalah format pilihan untuk pertukaran media digital antara perangkat, aplikasi, dan sistem operasi. File QT juga disimpan dalam format [MOV](/id/video/mov/) yang juga dikembangkan oleh Apple Inc. Beberapa aplikasi yang dapat membuka file QT antara lain Apple QuickTime player, VLC media player, dan Media Player Classic dengan K- Paket Codec Ringan.

## Format File QT

QTFF berorientasi objek yang memperlihatkan kumpulan objek yang fleksibel untuk kemudahan penguraian dan perluasan. Setiap trek dalam file QT berisi aliran media yang disandikan secara digital atau referensi data ke aliran media yang terletak di file lain. Struktur data hierarkis yang terdiri dari objek yang disebut atom bertindak sebagai wadah trek. Spesifikasi format file untuk [format file QT](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html) secara resmi tersedia oleh Apple Inc untuk referensi pengembang.

### Deskripsi media

Deskripsi media file QuickTime disimpan secara terpisah dari data media. Informasi seperti jumlah trek, format kompresi video, dan informasi waktu disimpan dalam deskripsi media (juga dikenal sebagai sumber film, atom film, atau hanya film). Data media dirujuk oleh indeks dalam struktur media ini. Data media adalah data sampel aktual, seperti frame video dan sampel audio, yang digunakan dalam film.

### Atom

Atom adalah unit dasar dari file QuickTime. Ada dua bidang utama dalam atom apa pun sebelum bidang lainnya: bidang Ukuran dan Jenis. Bidang ukuran menunjukkan ukuran atom sedangkan bidang jenis menunjukkan jenis data yang disimpan dalam atom. Secara alami, atom bersifat hierarkis yang berarti bahwa satu atom dapat berisi atom lain yang masih dapat memuat atom lainnya. Tata letak atom sampel ditunjukkan pada gambar berikut.

Setiap atom memiliki dua bagian, header, dan data. Header berisi bidang ukuran dan jenis dan bagian data berisi data aktual. Lebih lanjut, masing-masing bidang dijelaskan di bawah ini:

#### Ukuran Atom

Header dan konten atom ditunjukkan oleh bilangan bulat 32-bit yang dikenal sebagai ukuran atom. Bidang ukuran berisi ukuran atom dalam byte, dinyatakan dalam bilangan bulat tak bertanda 32-bit.

#### Jenis Atom

Jenis atom juga ditunjukkan oleh bilangan bulat 32-bit, yang sebagian besar diperlakukan sebagai bidang empat karakter dengan nilai knemonik, seperti 'moov' (0x6D6F6F76) untuk atom film, atau 'trak' (0x7472616B) untuk atom lintasan. Setelah jenis atom diketahui, ini memungkinkan untuk menafsirkan datanya.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Struktur File ##

File QT/MOV terdiri dari potongan berurutan. Setiap potongan memiliki header 8 byte: ukuran potongan 4-byte (big-endian, byte tinggi pertama) dan tipe potongan 4-byte - salah satu tanda tangan yang telah ditentukan sebelumnya: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "klip", "crgn", "sinkronisasi", "chap", "tmcd", "scpt", "ssrc", "PICT". Chunk pertama bertipe "ftype" dan memiliki sub-tipe di offset 8. MOV ditentukan oleh sub-tipe yang harus "qt". Untuk membuat file MOV, iterasi potongan diperlukan sampai tipe yang tidak diketahui terdeteksi.

Berikut ini contoh contohnya: Memeriksa data biner file MOV sampel, terbukti bahwa file tersebut dimulai dengan tanda tangan **ftyp** (hex: 66 74 79 70) pada offset 4, yang menentukan Jenis File Kontainer QuickTime. Sub-tipe file adalah **qt~_~_** (hex: 71 74 20 20) yang menunjuk ke tipe file MOV. Ukuran blok pertama adalah 32 (hex: 00 00 00 20, big-endian, high byte pertama), ukuran terletak di offset 0. Pada offset 32 (hex: 20) terletak blok kedua, yang berukuran 8 dan ketik **mdat** (hex: 6D 64 61 74).

Potongan berikutnya terletak di offset 32+8#40 (hex: 28) dan memiliki ukuran 3.263.028 (hex: 00 31 CA 34) dan ketik **mdat** (hex: 6D 64 61 74) pada offset 44 (hex : 2C). Potongan berikutnya terletak di offset 40 + 3.263.028#3.263.068 (hex: 00 31 CA 5C) dan memiliki ukuran 21.189 (hex: 00 00 52 C5) dan ketikkan **moov** (hex: 6D 6F 6F 76) pada offset 1.836.019.574 (hex: 00 31 CA 60). Ini adalah potongan terakhir, jadi total ukuran file adalah 3.263.068+21.189#3.284.257 byte.

## Referensi ##

* [Format File QT - Apple Inc.](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFPPreface/qtffPreface.html)
* [Format File QuickTime - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

