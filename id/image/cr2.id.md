{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File CR2 - File Gambar Canon Raw 2",
  "description":"Pelajari tentang format file CR2 dan API yang dapat membuat dan membuka file CR2.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Apa itu file CR2?

File CR2 (Camera RAW 2) adalah file gambar RAW yang dibuat oleh kamera digital Canon. Ini menyimpan data gambar lossless asli yang tidak diproses yang ditangkap oleh kamera. Format file CR2 dikembangkan oleh Canon untuk kamera digitalnya dan dapat merekam gambar berkualitas tinggi hingga 14 bit RGB. Ini menghasilkan gambar berkualitas tinggi dengan ruang pemrosesan pos yang cukup. Format gambar CR2 telah digunakan oleh Canon dalam model kamera 350D, 20D dan 1D mereka. File CR2 adalah file RAW dan berisi informasi metadata tambahan seperti informasi kamera, info lensa, informasi bracketing, white balance, dan pengaturan lainnya.

## Format File CR2

File CR2 disimpan ke kartu memori kamera sebagai file biner dalam format file milik Canon. Format file CR2 menggantikan format file CRW yang awalnya digunakan dan kemudian diganti dengan format file Canon RAW 3. Format file CR2 didasarkan pada spesifikasi [TIFF](/id/image/tiff/) yang memiliki 4 Direktori File Gambar (IFD).

|Offset |Konten |Komentar|
---|---|---|
|0x0000 |Header |berisi urutan byte, versi dan offset ke gambar RAW|
|computed |IFD#0 |bagian ini berisi bagian Exif, yang berisi bagian Makernotes.
Informasi tentang gambar#0|
|dihitung |gambar#0 |versi kecil gambar (seperempat ukuran aslinya), dikompresi dalam Jpeg|
|dihitung |IFD#1 |Informasi tentang gambar#1.|
|dihitung |gambar#1 |versi kecil dari gambar, dikompres dalam Jpeg|
|dihitung |IFD#2 |Informasi tentang gambar#2.|
|dihitung |gambar#2 |gambar versi kecil, tidak dikompresi|
|di tajuk| IFD#3| Informasi tentang gambar#3, gambar RAW dimensi penuh|
|dihitung |gambar#3 |Data gambar RAW, kompresi lossless dalam Jpeg (bukan data RGB!)|

## Keuntungan Format File CR2

Menyimpan gambar dalam format RAW memungkinkan banyak pemrosesan pasca foto seperti penyesuaian ke Keseimbangan Putih. Ini jauh lebih sulit dan dengan kehilangan kualitas yang besar dengan format file gambar lain seperti [JPEG](/id/image/jpeg/).

## Apakah CR2 lebih baik dari JPEG?

File CR2 adalah file mentah tanpa kehilangan data dan, karenanya, tidak ada penurunan kualitas. JPEG di sisi lain adalah format file gambar yang hilang karena kehilangan beberapa data untuk memperkecil file. Dengan demikian, file CR2 berkualitas tinggi dan lebih cocok untuk perbaikan dan penyempurnaan.

## Referensi

* [Format File CR2](http://lclevy.free.fr/cr2/)

