{
  "date" : "2021-04-08",
  "keywords" :[ "file lzma", "format file lzma", "apa itu file lzma", "file", "contoh lzma", "ekstensi file lzma", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - Format File Terkompresi LZMA",
  "description":"Apa itu file LZMA dan API yang dapat membuat dan membuka file LZMA.",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## Apa itu file LZMA?

File dengan ekstensi .lzma adalah file arsip terkompresi yang dibuat menggunakan metode kompresi LZMA (Lempel-Ziv-Markov chain Algorithm). Ini terutama ditemukan/digunakan pada sistem operasi Unix dan mirip dengan algoritme kompresi lain seperti [ZIP](/id/compression/zip/) untuk meminimalkan ukuran file. LZMA adalah format file lawas, yang sedang atau telah digantikan oleh format .xz. Jenis MIME dari format .lzma adalah \`application/x-lzma'. Format file ini dirancang oleh Igor Pavlov untuk digunakan di LZMA SDK.

## Format File LZMA

File LZMA terdiri dari dua bagian utama:

1. Tajuk
1. Data Terkompresi


### Tajuk LZMA

File LZMA memiliki header 13-byte yang diikuti oleh data terkompresi LZMA. Tajuk LZMA terdiri dari:

* Properti
* Ukuran Kamus
* Ukuran Tidak Terkompresi

#### Properti Header LZMA

Bidang Properti berisi tiga properti. Singkatan diberikan dalam tanda kurung, diikuti dengan rentang nilai properti. Lapangan terdiri dari

1) jumlah bit konteks literal (lc, [0, 8]);
2) jumlah bit posisi literal (lp, [0, 4]); dan
3) jumlah bit posisi (pb, [0, 4]).

#### Ukuran Kamus LZMA

Ini disimpan sebagai integer endian kecil 32-bit yang tidak ditandatangani dengan nilai mulai dari 2^n dan 2^n + 2^(n-1). Util LZMA dapat mendekompres file dengan ukuran kamus apa pun.

#### Ukuran Tidak Terkompresi
Ukuran Tidak Terkompresi disimpan sebagai bilangan bulat endian kecil 64-bit yang tidak ditandatangani. Nilai khusus 0xFFFF_FFFF_FFFF_FFFF menunjukkan bahwa Ukuran Tidak Terkompresi tidak diketahui. Nilai diwakili oleh End of Payload Marker (\*) jika dan hanya jika Uncompressed Size tidak diketahui.

## Referensi

* [Format File LZMA](https://svn.python.org/projects/external/xz-5.0.3/doc/lzma-file-format.txt)
* [Algoritme rantai Lempel–Ziv–Markov](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)

