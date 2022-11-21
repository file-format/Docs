{
  "date" : "2022-01-23",
  "keywords" :[ "file xz", "format file", "apa itu file xz", "file", "contoh xz", "ekstensi file xz", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File XZ - Arsip Terkompresi XZ",
  "description":"Pelajari tentang format file XZ dan API yang dapat membuat dan membuka file XZ.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## Apa itu file XZ?

XZ adalah format file terkompresi yang menggunakan algoritme kompresi LZMA2. Itu dirancang sebagai pengganti format gzip dan bzip2 yang populer, dan menawarkan sejumlah keunggulan dibandingkan standar lama ini. File XZ didukung dengan baik di banyak platform, dan dapat didekompresi dengan cepat dan mudah. Meskipun tidak umum seperti file [ZIP](/id/compression/zip/) atau [RAR](/id/compression/rar/), arsip XZ dapat digunakan untuk menyimpan data dalam jumlah besar tanpa mengorbankan kualitas kompresi. Jika Anda perlu mengompres atau mendekompres file besar, ekstensi file XZ patut dipertimbangkan.

## Format File XZ

File XZ dihasilkan dan disimpan sebagai file biner ke disk. Ini menggunakan algoritma LZMA untuk mengompresi data, dan dapat mencapai rasio kompresi hingga 50%. File XZ biasanya digunakan untuk distribusi perangkat lunak dan arsip cadangan. Mereka dapat didekompresi menggunakan utilitas XZ, yang disertakan di sebagian besar distribusi Linux.

## Buka zip File XZ di Linux/Unix

Untuk meng-unzip file XZ, instal paket `xz-utils` terlebih dahulu:
```
$ sudo apt-get install xz-utils
```

Gunakan perintah `unxz` untuk mengekstrak file .xz:
```
$ unxz compressed_xz_file.xz
```

atau menggunakan dengan opsi --decompress dari XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## Referensi

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)

