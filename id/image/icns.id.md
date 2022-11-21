{
  "date" : "2021-06-29",
  "keywords" :[ "ICNS", "ekstensi", "file", "format", "gambar", "Gambar Ikon Apple", "macOS", "Apple", "Ikon" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - Gambar Ikon Apple",
  "description":"Pelajari tentang format file ICNS dan API yang dapat membuat dan membuka file ICNS.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Apa itu berkas ICNS? ##

Format ikon yang digunakan oleh program macOS disebut file ICNS. Ini memungkinkan pita alfa 1-bit dan 8-bit dan menyimpan satu gambar atau lebih, biasanya dibuat dari dokumen [PNG](/id/image/png). Ikon program di browser dan antarmuka macOS ditampilkan menggunakan file ICNS.

Berdasarkan lokasinya, ikon gaya yang sama dapat memiliki beberapa setelan. Format ICNS telah mengalami banyak perubahan dan telah berkembang ke titik di mana sekarang dapat digunakan sebagai dasar untuk berbagai format yang kompatibel. Berikut adalah beberapa poin penting lainnya yang perlu Anda ketahui:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource, dan Mac OS icon Resource adalah beberapa nama lainnya.
* Untuk informasi ikon, sumber di cabang sumber digunakan.
* Dalam kebanyakan kasus, sebuah file berisi banyak gambar. 1612 piksel persegi dan 1024, 512, 256, 128, 48, 32, dan 16 piksel persegi mendukung ukuran gambar.


## Format File ICNS ##

Format data ICNS adalah kapsul untuk satu atau lebih gambar, mendukung pita 1-bit dan banyak status gambar.
Sistem operasi dapat mengubah ukuran gambar ikon agar sesuai dengan ukuran tampilan yang diperlukan. Gambar ikon yang lebih besar biasanya disimpan sebagai file [JPEG](/id/image/jpeg/) 2000 atau [PNG](/id/image/png). Jenis file ICNS terkompresi dan tidak terkompresi dimungkinkan.

Data header dan ikon biner membentuk struktur file ICNS. Header berisi 8 byte data, empat di antaranya adalah literal ajaib dan empat di antaranya adalah panjang file. Jenis dan ukuran setiap gambar ikon disimpan di bagian data ikon, yang diikuti oleh data gambar biner. Ukuran gambar menentukan ukuran bagian biner.

## Spesifikasi Teknis ##

### Tajuk ###

|Offset|Ukuran|Tujuan
---|---|---|
|0|4|Literal ajaib, harus berupa "icns" (0x69, 0x63, 0x6e, 0x73)
|4|4|Panjang file, dalam byte, msb terlebih dahulu


### Data ikon ###

|Offset|Ukuran|Tujuan
---|---|---|
|0|4|Jenis ikon
|4|4|Panjang data, dalam byte (termasuk tipe dan panjang), msb terlebih dahulu
|8|Variabel|Data ikon

### Kompresi ###

Data piksel dikompresi sampai batas tertentu. Piksel 32-bit ("is32", "il32", "ih32", "it32") dan ARGB ("ic04", "ic05") sering dikompresi (per saluran) dengan cara yang mirip dengan PackBits.

|Nilai Prospek|Byte Ekor|Hasil (tidak terkompresi)
---|---|---|
|0 - 127|1 - 128|1 - 128 Byte
|128 - 255|1 Byte|3 - 130 Salinan

## Referensi ##

* [ICNS - Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

