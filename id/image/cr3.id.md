{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File CR3 - File Gambar Canon Raw 3",
  "description":"Pelajari tentang format file CR3 dan API yang dapat membuat dan membuka file CR3.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Apa itu file CR3?

File CR3 adalah format file gambar Canon RAW yang dibuat oleh kamera digital Canon terpilih. Itu diperkenalkan oleh Canon untuk menggantikan format file CR2 dan digunakan oleh beberapa perangkat digital Canon. File CR3 menyimpan data gambar lossless asli yang tidak diproses yang ditangkap oleh kamera. Penggunaan gambar mentah ini memberikan gambar berkualitas tinggi dan memungkinkan banyak ruang untuk mengedit fotografer. Selain data gambar utama, file CR3 juga menyimpan informasi metadata tentang gambar tersebut.

## Format File CR3

File CR3 disimpan ke disk sebagai file biner dalam Format File Media Dasar ISO (ISO/IEC 14496-12) dan juga menyertakan [tag Canon](https://exiftool.org/TagNames/Canon.html#uuid) khusus. Ini juga termasuk [codec Canon 'crx'](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) yang merupakan campuran dari JPEG-LS (Rice-Golomb + RLE coding) dan JPEG-2000 (LeGall 5/3 DWT + kuantifikasi).

## Tag Kustom CR3

File CR3 berisi tag khusus untuk berbagai tujuan. Beberapa tag tersebut adalah sebagai berikut.

|Tag ID| Nama Tag| Dapat ditulisi |Nilai / Catatan|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Tag CCTP Canon|
|'CMT1' |IFD0| - |--> Tag EXIF|
|'CMT2' |ExifIFD| - |--> Tag EXIF|
|'CMT3' |MakerNoteCanon| - |--> Tag Canon|
|'CMT4' |GPSInfo| - |--> Tag GPS|
|'CNCV' |CompressorVersion| tidak| |
|'CNOP' |CanonCNOP| - |--> Tag Canon CNOP|
|'CNTH' |CanonCNTH| - |--> Tag Canon CNTH|
|'THMB' |ThumbnailImage| tidak| |

## Referensi

* [Format File CR2](http://lclevy.free.fr/cr2/)
* [Tag Canon](https://exiftool.org/TagNames/Canon.html#uuid)

