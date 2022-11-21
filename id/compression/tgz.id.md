{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File TGZ - File Tar Gzip",
  "description":"Pelajari tentang format file TGZ dan API yang dapat membuat dan membuka file TGZ.",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## Apa itu file TGZ?

File dengan ekstensi .tgz adalah file arsip TAR, terdiri dari beberapa file dan folder, yang telah dikompresi menggunakan perangkat lunak kompresi Gnu Zip (gzip). File [TAR](/id/compression/tar/) biasanya menggabungkan beberapa file menjadi satu file untuk cadangan atau distribusi melalui internet. Ini adalah file uncompress sampai dikompresi menggunakan perangkat lunak gzip setelah itu menjadi file TGZ. File TGZ, sebagai file terkompresi, memakan lebih sedikit ruang pada disk dan mudah ditransfer menggunakan internet melalui email. Beberapa aplikasi yang bisa membuka file TGZ antara lain WinZip, Apple Archive Utility, 7-Zip, dan WinRAR. File TGZ sebagian besar digunakan dalam sistem UNIX dan Linux.

## Format File TGZ

File TGZ disimpan sebagai file biner terkompresi menggunakan algoritme kompresi [GZ](/id/compression/gz/).

## Cara membongkar file .tgz di Linux

Di Linux/Unix OS, perintah berikut dapat digunakan untuk mengekstrak file TGZ dari baris perintah.

```
tar zxvf tgzCompressedFile.tgz
```

Perintah di atas mendekompresi file TGZ terkompresi dan mengekstrak file-nya dari arsip TAR ke disk.
## Referensi ##

* [TGS](https://core.telegram.org/animated_stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

