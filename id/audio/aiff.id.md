{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "file", "ekstensi", "format", "format file pertukaran audio", "musik", "format file aiff", "aiff ke mp3", "aiff vs wav", "ubah aiff ke mp3" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file AIFF dan API yang dapat membuat, mengonversi, dan membuka file AIFF.",
  "title" :"AIFF - Format File Pertukaran Audio",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Apa itu file AIFF?
AIFF (Audio Interchange File Format) adalah format file audio tidak terkompresi yang dikembangkan oleh Apple pada tahun 1998, tetapi didasarkan pada **EA IFF 85** (Standar untuk File Format Interchange yang dikembangkan oleh Electronic Arts), format pembungkus yang digunakan pada sistem Amiga . Format file ini muncul dengan standar untuk menyimpan sampel suara. Formatnya cukup baik dalam hal fleksibilitas, dan memungkinkan penyimpanan sampel suara monaural atau multisaluran pada berbagai laju sampel dan lebar sampel. Karena file AIFF tidak dikompresi, hal ini membuat ukurannya lebih besar daripada format lossy lainnya seperti [MP3](/audio/mp3/).

File AIFF terdiri dari 2 saluran audio stereo tidak terkompresi dengan ukuran sampel 16 bit, direkam pada 44,1 khz. Karena audio berkualitas tinggi, audio 5 menit dapat memakan ruang disk hingga 50 MB yang mirip dengan format file [WAV](/audio/wav/).

## AIFF vs WAV

AIFF dan WAV memiliki kualitas yang hampir sama. Keduanya menggunakan pengkodean PCM (pulse-code modulation) yang sama, yang membuatnya berukuran lebih besar dibandingkan dengan format lossy lainnya, seperti, [MP3](/audio/mp3/), [M4A](/audio/m4a/). Beberapa perbedaan umum ditulis dalam tabel di bawah ini:

|AIFF|WAV|
---|---|
|Sebagian besar digunakan untuk MAC|Sebagian besar digunakan untuk PC|
|Memungkinkan metadeta| Tidak mengizinkan metadeta|

## Struktur File AIFF

**EA IFF 85** menetapkan struktur keseluruhan untuk menyimpan data dalam file. File **EA IFF 85** terdiri dari sejumlah potongan data. Sebuah chunk sedang membangun blok file AIFF terdiri dari beberapa informasi header diikuti oleh data:
{{< figure src="../chunk.png" alt="Potongan AIFF" >}}

File AIFF adalah kumpulan dari sejumlah jenis potongan yang berbeda. Ada dua jenis potongan umum yang penting untuk membentuk potongan file AIFF:
- **Common Chunk**: Berisi parameter penting yang menjelaskan sampel suara, seperti panjang dan laju sampel.
- **Potongan Data Suara**: Berisi sampel audio sebenarnya.
Ada banyak potongan opsional lainnya yang mencantumkan parameter instrumen, menentukan penanda, menyimpan informasi khusus aplikasi, dll.

### Jenis Potongan Lokal

Jenis potongan untuk membentuk AIFF diberikan dalam tabel di bawah ini:

|Jenis Potongan| Deskripsi|
---|---|
|Common Chunk|Common Chunk menjelaskan parameter fundamental dari sampel suara|
|Potongan Data Suara|Potongan Data Suara berisi bingkai sampel aktual|
|Potongan Marker|Potongan Marker berisi penanda yang menunjuk ke posisi dalam data suara|
|Instrument Chunk|Instrument Chunk mendefinisikan parameter dasar yang dapat digunakan instrumen, seperti sampler, untuk memutar ulang data suara|
|Potongan Data MIDI|Potongan Data MIDI dapat digunakan untuk menyimpan data MIDI|
|Potongan Rekaman Audio|Potongan Rekaman Audio berisi informasi yang berkaitan dengan perangkat perekam audio|
|Potongan Khusus Aplikasi|Potongan Khusus Aplikasi dapat digunakan untuk tujuan apa pun oleh produsen aplikasi|
|Comments Chunk|Comments Chunk digunakan untuk menyimpan komentar pada FORM AIFF|
|Potongan Teks - Nama, Pengarang, Hak Cipta, Anotasi| Semuanya adalah potongan teks|

## Referensi ##

* [Format File Pertukaran Audio - Oleh Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

