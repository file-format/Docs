{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Video Audio Terkompresi", "File", "Ekstensi", "Format File", "Kontainer Multimedia", "XVid", "DivX", "Codec", "Format File Pertukaran Sumber Daya", "RIFF "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File AVI - File Audio Video Interleave",
  "description":"Pelajari tentang format file AVI dan API yang dapat membuat dan membuka file AVI.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## Apa itu file AVI? ##

Format file **AVI** adalah format file wadah multimedia Audio Video yang diperkenalkan oleh Microsoft. Itu menyimpan data audio dan video yang dibuat dan dikompresi menggunakan beberapa codec (Coder/Decoder) seperti **XVid** dan **DivX**. Karena codec yang berbeda dapat digunakan untuk menyandikan konten AVI, aplikasi pengambilan yaitu pemutar AVI, harus dapat membuka ini hanya jika mereka memiliki codec yang diperlukan yang diinstal dengan konten AVI yang dibuat. Format ini didukung secara default di semua platform **Microsoft Windows** serta di hampir semua platform utama lainnya. Beberapa aplikasi dan API menyediakan kemampuan untuk membuat/menyimpan, membaca, dan mengonversi AVI ke format populer lainnya seperti MP4, MOV, WMV, dll.

## Format File AVI ##

File yang memiliki ekstensi .avi adalah file AVI. Ini adalah sub-format dari Resource Interchange File Format (RIFF). RIFF mengatur data ke dalam blok, atau "potongan", yang diidentifikasi dengan tag FourCC. File AVI hanyalah satu "potongan" dalam file berformat RIFF.

Di sub-bagian pertama, tajuk file diidentifikasi dengan tag "hdrl"; isinya termasuk lebar, tinggi, dan frekuensi gambar video. Di sub-bagian kedua, tag gerak mewakili frekuensi gambar video. Video AVI terdiri dari data audio/visual aktual dalam bagian ini. Ada juga subchunk opsional ketiga dengan tag "idx1", yang menunjukkan posisi dalam file dari masing-masing potongan data milik file tersebut.

### Keterbatasan ###

* Informasi rasio aspek tidak dapat dikodekan dalam spesifikasi AVI asli, meskipun spesifikasi OpenDML selanjutnya (AVI 2.0) menawarkan metode standar
* Meskipun file AVI digunakan secara luas dalam pascaproduksi film dan televisi, berbagai pendekatan untuk menambahkan kode waktu ke file tersebut bersaing, memengaruhi kegunaan format.
* File video yang disandikan dalam AVI tidak dapat menggunakan teknik kompresi yang membutuhkan data bingkai di masa mendatang di luar bingkai yang sedang disandikan (B-frame)
* Bermasalah jika menggunakan file AVI dengan kecepatan bit variabel (VBR) (seperti audio MP3 dengan kecepatan sampel di bawah 32 kHz)
* Film fitur definisi standar penyandian file AVI seperti yang biasa digunakan kemungkinan akan menimbulkan biaya overhead sekitar 5 MB per jam, tergantung pada bagaimana file tersebut digunakan
* Subtitle harus di-hardcode ke dalam aliran video atau didistribusikan dalam file terpisah jika file AVI tidak dapat menampung lampiran seperti font dan subtitle

## Sejarah Singkat ##

AVI diperkenalkan oleh Microsoft pada tahun 1992 dengan tujuan untuk menyediakan format file audio dan video yang lebih kuat dan canggih. Formatnya dengan cepat menjadi populer dengan penggunaan internet, memungkinkan individu untuk berbagi file video secara langsung dan tidak langsung melalui penyimpanan media berbasis cloud.

## Referensi ##

* [AVI - Oleh Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

