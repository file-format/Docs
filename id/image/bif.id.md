{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "File BIF - Format Gambar Seluruh Slide Ventana",
  "description":"Pelajari tentang format file BIF dan API yang dapat membuat dan membuka file BIF.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif-id",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Apa itu file BIF?

File BIF adalah file gambar raster yang berisi gambar spesimen slide. Ini terdiri dari beberapa gambar TIFF yang digabungkan dengan aplikasi tampilan slide menjadi satu gambar komposit. File BIF dibuat oleh pemindai slide digital sistem Ventana Medical dan sepenuhnya sesuai dengan varian BigTIFF dari definisi [TIFF](/image/tiff/) v 6.0.

## Format File BIF

File BIF disimpan sebagai file gambar biner dan terdiri dari sebanyak 200.000 x 200.000 piksel. Hal ini dapat menyebabkan ukuran file menjadi besar, melanggar batas ukuran 4 GB yang diberlakukan oleh penunjuk file 32-bit yang ditentukan oleh standar TIF. Namun, dengan penunjuk file 64-bit, hambatan ukuran file ini diatasi dengan varian BigTIFF dari standar TIFF.

### Siapa yang menggunakan File BIF?

File BIF digunakan oleh pemindai slide digital untuk memindai dan membuat salinan digital spesimen slide. Jika Anda seorang Ahli Patologi, Anda dapat membuka file BIF ini dalam aplikasi tampilan slide. Dengan tingkat detail yang tinggi dan data beresolusi tinggi, Anda dapat memperbesar dan memperkecil gambar slide untuk melihat bagian spesimen dengan lebih atau kurang detail. File metadata [XML](/web/xml/) yang ada dalam file ini menentukan cara menggabungkan gambar, dan gambar yang harus digunakan sebagai thumbnail file.

## Bagaimana Cara Membuka File BIF?

Anda dapat membuka file BIF dengan:

 * OpenSlide (lintas platform)
 * ImageJ (lintas platform)
 * Penampil NetScope (Windows)

## Referensi ##

 * [Buku Putih BIF Patologi Digital Roche](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

