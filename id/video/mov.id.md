{
  "date" : "2019-10-11",
  "keywords" :[ "file mov", "format file mov", "apa itu file mov", "file", "contoh mov", "ekstensi file mov", "ekstensi", "format", "QuickTime", "MPEG- 4"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File MOV - Format File Film Apple QuickTime",
  "description":"Pelajari tentang format file MOV dan API yang dapat membuat dan membuka file MOV.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## Apa itu file MOV?

File MOV adalah jenis file video, yang dikembangkan oleh Apple Inc., yang berisi satu atau lebih trek. Setiap trek menyimpan film, audio, klip film, dan subtitle. Ini adalah wadah multimedia yang dapat menyimpan berbagai jenis elemen media. Format video MOV kompatibel dengan sistem Windows dan Macintosh. Ini menggunakan kode MPEG-4 untuk kompresi dan trek dipertahankan dalam objek yang disebut atom yang ditempatkan dalam struktur data hierarkis.

## Sejarah Singkat Format File MOV

Format file MPEG-4 telah berevolusi dari spesifikasi QuickTime File Format (**QTFF**) pada tahun 2001. Organisasi Standardisasi Internasional menyetujui format tersebut dan spesifikasi sistem MPEG-4 Bagian 1 diterbitkan pada tahun 1999. Pada tahun 2001, file revisi format [MP4](/id/video/mp4/) diterbitkan.

Versi pertama MP4 direvisi pada tahun 2003 sebagai MPEG-4 Part 14 (ISO/IEC 14496-14:2003). Pada tahun 2004, MP4 digeneralisasi untuk mendefinisikan struktur umum untuk semua file media berbasis waktu. Oleh karena itu, sekarang digunakan sebagai dasar untuk berbagai format file multimedia lainnya.

## Format File QuickTime (QTFF) - Informasi Lebih Lanjut

Untuk bekerja dengan multimedia digital, QTFF dapat menyimpan banyak jenis data. Ini adalah format ide untuk pertukaran media digital karena format tersebut menentukan standar untuk menggambarkan segala jenis struktur media. Format file terdiri dari kumpulan objek berorientasi objek yang fleksibel. Untuk penyimpanan film pada disk, QuickTime menggunakan dua struktur yaitu `atoms` dan `atom QT`.

### Atom

Atom adalah unit dasar dari file QuickTime. Ada dua bidang utama dalam atom apa pun sebelum bidang lainnya: bidang Ukuran dan Jenis. Bidang ukuran menunjukkan ukuran atom sedangkan bidang jenis menunjukkan jenis data yang disimpan dalam atom. Secara alami, atom bersifat hierarkis yang berarti bahwa satu atom dapat berisi atom lain yang masih dapat memuat atom lainnya. Tata letak atom sampel ditunjukkan pada gambar berikut.

Setiap atom memiliki dua bagian, `header`, dan `data`. Header berisi bidang ukuran dan jenis dan bagian data berisi data aktual. Lebih lanjut, masing-masing bidang dijelaskan di bawah ini:

### Ukuran Atom

Header dan konten atom ditunjukkan oleh bilangan bulat 32-bit yang dikenal sebagai ukuran atom. Bidang ukuran berisi ukuran atom dalam byte, dinyatakan dalam bilangan bulat tak bertanda 32-bit.

### Jenis Atom

Jenis atom juga ditunjukkan oleh bilangan bulat 32-bit, yang sebagian besar diperlakukan sebagai bidang empat karakter dengan nilai knemonik, seperti 'moov' (0x6D6F6F76) untuk atom film, atau 'trak' (0x7472616B) untuk atom lintasan. Setelah jenis atom diketahui, ini memungkinkan untuk menafsirkan datanya.

### Atom QT dan Kontainer Atom

Atom QT menyediakan format penyimpanan tujuan umum dan memiliki header tambahan yang terdiri dari bidang Ukuran, Jenis, ID Atom, dan Jumlah atom Anak. Atom QT dibungkus dalam wadah atom, struktur data unik yang memiliki header dengan jumlah kunci. Ada satu atom akar di setiap wadah atom yang merupakan atom QT. Tata letak atom QT ditunjukkan pada gambar di bawah ini.

Header wadah atom QT memiliki data berikut:

Dicadangkan: Elemen 10 byte dengan nilai 0.

Jumlah Kunci: bilangan bulat 16-bit dengan nilai 0.

Header atom QT memiliki data berikut:

**Ukuran -** Tajuk dan konten atom QT ditunjukkan dalam byte dengan bilangan bulat 32-bit. Dalam kasus atom daun, maka bidang ini berisi ukuran atom tunggal.

**Jenis -** Jenis atom ditunjukkan dengan bilangan bulat 32-bit. Jika itu adalah atom akar, maka nilainya disetel ke 'sean'.

**ID Atom -** Ini adalah bilangan bulat 32-bit yang menunjukkan ID atom dan harus unik untuk semua saudara. Root atom selalu nilai atom ID sebagai 1.

**Dicadangkan -** Bilangan bulat 16-bit yang harus disetel ke 0.

**Jumlah anak -** Bilangan bulat 16-bit yang menunjukkan jumlah anak atom dari sebuah atom.

**Dicadangkan -** Bilangan bulat 32-bit yang harus disetel ke 0.

## Struktur File File MOV

File MOV terdiri dari potongan berurutan. Setiap potongan memiliki header 8 byte: ukuran potongan 4-byte (big-endian, byte tinggi pertama) dan tipe potongan 4-byte - salah satu tanda tangan yang telah ditentukan sebelumnya: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "klip", "crgn", "sinkronisasi", "chap", "tmcd", "scpt", "ssrc", "PICT". Chunk pertama bertipe "ftype" dan memiliki sub-tipe di offset 8. MOV ditentukan oleh sub-tipe yang harus "qt". Untuk membuat file MOV, iterasi potongan diperlukan sampai tipe yang tidak diketahui terdeteksi.

Berikut adalah `contoh contoh`: Memeriksa data biner file MOV sampel, terbukti bahwa file tersebut dimulai dengan tanda tangan **ftyp** (hex: 66 74 79 70) pada offset 4, yang menentukan Jenis File Kontainer QuickTime. Sub-tipe file adalah **qt~_~_** (hex: 71 74 20 20) yang menunjuk ke tipe file MOV. Ukuran blok pertama adalah 32 (hex: 00 00 00 20, big-endian, high byte pertama), ukuran terletak di offset 0. Pada offset 32 (hex: 20) terletak blok kedua, yang berukuran 8 dan ketik **mdat** (hex: 6D 64 61 74).

Potongan berikutnya terletak di offset 32+8#40 (hex: 28) dan memiliki ukuran 3.263.028 (hex: 00 31 CA 34) dan ketik **mdat** (hex: 6D 64 61 74) pada offset 44 (hex : 2C). Potongan berikutnya terletak di offset 40 + 3.263.028#3.263.068 (hex: 00 31 CA 5C) dan memiliki ukuran 21.189 (hex: 00 00 52 C5) dan ketikkan **moov** (hex: 6D 6F 6F 76) pada offset 1.836.019.574 (hex: 00 31 CA 60). Ini adalah potongan terakhir, jadi total ukuran file adalah 3.263.068+21.189#3.284.257 byte.

## Bagaimana Cara Mengonversi File MOV?

Ada banyak pemutar media dan editor video perangkat lunak yang tersedia untuk mengonversi file MOV ke format file video populer lainnya. Beberapa pemutar media yang dapat mengonversi file MOV ke format lain antara lain:

* Pemutar media VLC VideoLAN
* Pemutar Eltima Elmedia

Beberapa pemutar media dan editor video, termasuk pemutar media VideoLAN VLC dan Eltima Elmedia Player, dapat mengonversi file MOV ke format lain. Perangkat lunak ini dapat mengonversi file MOV ke format video berikut.

* Video MPEG-4 - [MP4](/id/video/mp4/)
* Video WebM - [WEBM](/id/video/webm/)
* Aliran Transportasi Video - [TS](/id/video/ts/)
* Format Sistem Lanjutan - [ASF](/id/video/ts/)
* Ogg Vorbis Audio - [OGG](/id/audio/ogg/)
* Audio MP3 - [MP3](/id/audio/mp3/)
* Codec Audio Lossless Gratis - [FLAC](/id/audio/flac/)
* GELOMBANG Audio - [WAV](/id/audio/wav/)

## Open Source API untuk File MOV

* [React Native API untuk mengonversi MOV ke MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [Python API untuk memperbaiki File MOV](https://github.com/nrosenstein-stuff/movrepair)
* [API Ruby untuk mengonversi MOV ke GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## Referensi

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

