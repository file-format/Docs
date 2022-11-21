{
  "date" : "2019-12-09",
  "keywords" :[ "file zl", "format file zl", "apa itu file zl", "file", "contoh zl", "ekstensi file zl", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - Format File Terkompresi ZLIP",
  "description":"Pelajari tentang format file ZL dan API yang dapat membuat dan membuka file ZL.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## Apa itu file ZL?

File dengan ekstensi .zl adalah format file terkompresi ZLIP yang menggunakan varian algoritma kompresi DEFLATE untuk mengompresi file. Ini tidak tergantung pada jenis CPU, sistem operasi, sistem file, dan kumpulan karakter, dan karenanya dapat digunakan untuk pertukaran informasi. Spesifikasi teknis kompresi ZLIP tersedia di [situs IETF](https://tools.ietf.org/html/rfc1950) dan dapat dirujuk dari sudut pandang developer.

## Format File ZL

Aliran zlib memiliki struktur berikut:

* `CMF (Compression Method and flags)` - byte ini dibagi menjadi metode kompresi 4-bit dan bidang informasi 4-bit tergantung pada metode kompresi.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (Metode kompresi)` - Ini mengidentifikasi metode kompresi yang digunakan dalam file. Nilai-nilainya dan metode kompresi yang sesuai adalah sebagai berikut.

| Nilai CM| Kompresi|
|---|---|
|CM = 8|DEFLATE dengan ukuran jendela hingga 32K|
|CM = 15|Dicadangkan|

* `CINFO (Compression info)` - Untuk CM = 8, CINFO adalah logaritma basis-2 dari ukuran jendela LZ77, minus delapan (CINFO=7 menunjukkan ukuran jendela 32K).

* `FLG (FLaGs)` - byte bendera ini dibagi sebagai berikut:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Referensi ##

* [Spesifikasi Format File Zlib](https://tools.ietf.org/html/rfc1950)

