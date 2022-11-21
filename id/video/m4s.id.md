{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File M4S - Apa itu file M4S?",
  "description":"Pelajari tentang format file M4S dan API yang dapat membuat dan membuka file M4S.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## Apa itu file M4S?

File M4S adalah segmen kecil dari video yang dialirkan melalui internet menggunakan teknik streaming **MPEG-DASH**. Ini berisi segmen video dalam bentuk data biner. Aplikasi penerima (biasanya browser web atau pemutar media) memutar segmen ini sesuai urutan penerimaannya. Segmen M4S pertama diidentifikasi oleh data inisialisasi yang dikandungnya. Dalam **ringkasan**, file M4S adalah segmen media individual kecil dari file lengkap.

## Format File M4S

File M4S didasarkan pada [format File Media Dasar ISO (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Segmen kecil dari file besar ini dapat diunduh secara terpisah melalui HTTP. Jadi, jika Anda memiliki file film [MP4](/id/video/mp4/) yang besar, file tersebut dapat dialirkan menggunakan teknik MPEG-DASH (Dynamic Adaptive Streaming over HTTP) dengan mengelompokkannya sebagai file segmen M4S. Jika file film besar ini diunduh ke disk sebagai M4S, beberapa file M4S diunduh. Jika semua segmen .m4s ini digabungkan, file lengkap yang dapat diputar dihasilkan. Pemutar media tidak dapat memutar file kecuali segmen inisialisasi pertama juga tersedia dengan file tersebut.

## Tentang Streaming MPEG-DASH

MPEG-DASH menggunakan teknik streaming kecepatan bit adaptif yang memungkinkan streaming konten media berkualitas tinggi melalui internet. Ini dilakukan dengan memecah konten menjadi urutan segmen kecil yang dialirkan melalui HTTP. File media besar seperti film, podcast, atau siaran langsung acara olahraga dapat dialirkan dengan cara ini. Segmen ini dikodekan pada kecepatan bit yang berbeda. Pemutar media berkemampuan MPEG-DASH secara otomatis memilih segmen dengan laju bit tertinggi menggunakan algoritme adaptasi laju bit. Hal ini untuk menghindari penundaan atau penyanggaan ulang peristiwa dalam pemutaran.

### Open-Source API untuk file M4S

Ada API sumber terbuka yang tersedia yang dapat digunakan untuk membaca dan mengonversi file M4S.

* [libdash](https://github.com/bitmovin/libdash) - .NET API untuk file M4S
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - klien Javascript untuk file M4S
* [Go Library untuk membuat File Dash](https://github.com/zencoder/go-dash)

### Open-Source API untuk Mengonversi M4S ke MP4

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Referensi ###

* [Format File Media Berbasis ISO (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [Streaming Adaptif Dinamis melalui HTTP - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

