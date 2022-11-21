{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "file", "ekstensi", "format", "MPEG-4", "Manajemen Hak Digital", "DRM", "Apple", "video"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"Pelajari tentang format file M4V dan API yang dapat membuat dan membuka file M4V.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## Apa itu file M4V?

Format file **M4V**, yang dikembangkan oleh Apple, adalah wadah video yang secara opsional dilindungi dengan perlindungan salinan Digital Rights Management (DRM) untuk melindungi privasi atau salinan. Video dan trek audio dibungkus oleh file kontainer untuk mengindeks dan mengatur aliran pemutaran. Selain itu, wadah juga menyediakan fitur bab yang mirip dengan yang ada di DVD. Apple menggunakan M4V untuk menyandikan video di iTunes Store-nya. Ini melindungi reproduksi tidak sah melalui perlindungan salinan FairPlay Apple dengan mengizinkan file M4V diputar hanya di komputer resmi yang memiliki akun yang digunakan untuk membeli video. Namun, jika perlindungan DRM dihapus dari file M4V, file ini dapat diputar di pemutar video lain dengan mengubah ekstensi dari .m4v menjadi .mp4, itulah sebabnya file M4V dikaitkan dengan MPEG-4. M4V menggunakan H.264 untuk video dan **[AAC](/id/audio/aac/)** dan Dolby Digital untuk encoding dan decoding audio.

## Struktur File M4V ##

File M4V memiliki potongan kontinu dengan header 8 byte, ukuran potongan 4 byte, dan tipe potongan 4 byte di setiap potongan. Chunk pertama adalah “ftype” dan memiliki sub-tipe pada offset 8. M4V ditentukan oleh sub-tipe yang harus "M4V_". Jenis potongan lebih lanjut adalah tanda tangan yang telah ditentukan sebelumnya: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide" , "memuat", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " PICT". Iterasi potongan, hingga tipe yang tidak diketahui terdeteksi, kami membuat file M4V.

Berikut adalah pemeriksaan sampel: Data biner file m4v sampel diperiksa melalui Hex Viewer dan dapat diamati bahwa itu dimulai dengan tanda tangan **ftyp** (hex: 66 74 79 70) pada offset 4, yang menentukan QuickTime Jenis File Kontainer. Sub-tipe file adalah **M4V_** (hex: 4D 34 56 20) yang menunjuk ke tipe file M4V (MPEG-4). Ukuran blok pertama adalah 32 (hex: 00 00 00 20, big-endian, high byte pertama), ukuran terletak di offset 0. Pada offset 32 (hex: 20) terletak blok kedua, yang berukuran 30.322 (hex : 00 00 76 72, big-endian, byte rendah dulu) dan ketik **moov** (hex: 6D 6F 6F 76). Potongan berikutnya terletak di offset 32+30,322#30,354 (hex: 00 00 76 92) dan memiliki ukuran 8 (hex: 00 00 00 08) dan tipe **free** (hex: 66 72 65 65).
### Codec Digunakan di M4V ###

#### Kodek Video H.264 ####

H.264 adalah standar kompresi video yang mengubah video digital menjadi format yang membutuhkan lebih sedikit ruang saat diperlukan transmisi atau penyimpanan. M4V menggunakan H.264 untuk kompresi video. Aplikasinya berkisar dari DVD, TV, Videoconference, dan video streaming melalui internet. H.264 terdiri dari dua bagian utama: Encoder – Yang memampatkan video, Decoder – Yang membuka kompresi kembali video yang dikompresi. Pada gambar di bawah, proses encoding dan decoding disorot, dan proses lainnya tercakup dalam standar H.264.

##### Proses Coding dan Decoding Video di H.264 #####

Untuk bitstream H.264 terkompresi, encoder video melakukan proses prediksi, transformasi, dan encoding. Pada saat yang sama, decoder melakukan proses kebalikan dari decoding, inverse transform, dan rekonstruksi untuk menghasilkan kembali file video. H.264 membutuhkan setengah ukuran MPEG.

#### Kodek Audio ####

Advanced Audio Coding (AAC) adalah codec audio untuk kompresi audio digital lossy dan digunakan dalam wadah M4V. AAC adalah penerus format [MP3](/id/audio/mp3/) dan mencapai kualitas yang lebih baik daripada MP3 dengan kecepatan bit yang sama. Format AAC membuang beberapa informasi selama proses kompresi, yang kurang penting. AAC adalah codec berbasis blok kecepatan bit variabel (VBR) di mana setiap blok diterjemahkan ke 1024 sampel domain waktu.

### Referensi ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipedia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

