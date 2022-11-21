{
  "date" : "2021-06-16",
  "keywords" :[ "LZH", "Terkompresi", "File", "Ekstensi", "Format File", "Lempel-Ziv", "Haruyasu", "LHA" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File LZH",
  "description":"Pelajari tentang format file LZH dan API yang dapat membuat dan membuka file LZH.",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Apa itu file LZH? ##

File dengan ekstensi .lzh dan .lha biasanya berhubungan dengan format file kompresi arsip. Format file ini sama dengan format kompresi file lainnya seperti [ZIP](/id/compression/zip/), [RAR](/id/compression/rar/), dll. Tujuan utama dari format file ini adalah untuk memperkecil ukuran file format agar mudah dikirim serta untuk menyatukannya dalam bentuk terkompresi. SEBAGAI dibandingkan dengan perusahaan barat lainnya, file LZH sangat populer di Jepang dan biasanya digunakan untuk mengompresi data video game. Add-on LZH untuk Windows 7 dibangun ke dalam Windows 7 versi Jepang. Microsoft pertama kali merilis Add-on Folder Microsoft Compressed (LZH) untuk Windows XP versi Jepang. Format file ini diimplementasikan dengan ketentuan kompresi dan fitur yang digunakan oleh algoritma Lempel-Ziv dan Haruyasu

## Spesifikasi LZH ##

Metode kompresi arsip LZH ditampilkan sebagai string teks lima byte, seperti -lz1-. Ini adalah byte ketiga hingga ketujuh dalam file terkompresi.

|Spesifikasi|Deskripsi|
---|---|
|Ekstensi | .lzh, .lha|
|Jenis Media| aplikasi/x-lzh-terkompresi|
|Ketik Kode| "LHA_" (LHA-SPACE)|
|UTI| public.archive.lha|
|Dikembangkan Oleh| Haruyasu Yoshizaki (Yoshi)|
|Tipe| Kompresi|
|Diperpanjang dari| LArc|

## Masalah untuk Membuka file LZH ##

Berikut adalah beberapa masalah yang dapat menyebabkan format file LZH tidak berfungsi dengan baik:
  

* File mungkin rusak. Untuk mengatasi masalah ini, unduh file lagi atau minta pengirim untuk mengirim ulang file lagi
* Alasan kedua adalah file yang terinfeksi dalam hal ini memindai file dengan benar
* Tautan yang salah ke file LZH
* Penghapusan deskripsi LZH
* Tidak cukup sumber daya perangkat keras
* Pengemudi peralatan yang ketinggalan jaman

## Referensi ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
