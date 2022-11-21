{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Terkompresi", "File", "Ekstensi", "Format File", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File LZO",
  "description":"Pelajari tentang format file LZO dan API yang dapat membuat dan membuka file LZO.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Apa itu file LZO? ##

File dengan ekstensi .lzo digabungkan dengan fitur pengarsipan file yang dapat memperkecil semua ukuran file dalam file terkompresi. Semua file terkompresi dapat terdiri dari satu atau lebih file atau bahkan grup pengikat dengan beberapa file dengan jenis dan dimensi yang berbeda. Ukuran file terkompresi lebih kecil dibandingkan dengan ukuran gabungan semua file dan folder yang disimpan dalam file terkompresi LZO. Semua file terkompresi LZO disimpan dalam format LZO dan dieksekusi secara eksplisit dengan fitur kompresi yang digunakan oleh perangkat lunak kompresi dan dekompresi file LZOP. Semua spesifikasi kompresi digabungkan ke dalam program kompresi dan dekompresi file ini yang berasal dari pustaka kompresi file Lempel-Ziv-Oberhume. Kecepatan dekompresi yang lebih cepat dan rasio kompresi yang dikembangkan juga digabungkan ke dalam file LZO ini.

## Spesifikasi LZO ##

Markus Franz Xaver Johannes Oberhumer mengembangkan algoritme "lzop" asli, berdasarkan algoritme sebelumnya oleh Abraham Lempel dan Jacob Ziv, pada tahun 1996. Perpustakaan ini mengimplementasikan berbagai algoritme dengan karakteristik sebagai berikut:

* Kompresi lebih cepat daripada DEFLATE
* Dekompresi cepat
* Buffer tambahan yang diperlukan selama kompresi (berukuran 8KB atau 64KB, bergantung pada tingkat kompresi)
* Buffer sumber dan tujuan adalah semua memori yang diperlukan untuk dekompresi
* Memberikan kontrol atas rasio kompresi dan kecepatan kompresi

Sebagai algoritme kompresi blok, LZO melakukan kompresi yang tumpang tindih serta dekompresi di tempat. Untuk mencapai kompresi yang tumpang tindih, ukuran blok kompresi dan dekompresi harus sama. Algoritme kompresi LZO membagi data input menjadi kecocokan (kamus geser) dan literal yang tidak cocok, memberikan hasil yang baik dengan data yang sangat redundan dan hasil yang dapat diterima dengan data yang tidak dapat dikompresi, hanya meningkatkan data yang tidak dapat dikompresi sebesar 1/64 dari aslinya ukuran.

## Masalah untuk Membuka file LZO ##

Berikut adalah beberapa masalah yang dapat menyebabkan format file LZO tidak berfungsi dengan baik:
  


* File mungkin rusak. Untuk mengatasi masalah ini, unduh file lagi atau minta pengirim untuk mengirim ulang file lagi
* Alasan kedua adalah file yang terinfeksi dalam hal ini memindai file dengan benar
* Tautan yang salah ke file LZO
* Penghapusan deskripsi LZO
* Tidak cukup sumber daya perangkat keras
* Pengemudi peralatan yang ketinggalan zaman
  


## Referensi ##

* [LZO - Oleh Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

