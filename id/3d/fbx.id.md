{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "file", "ekstensi", "format", "Format File 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Panduan format file Anda untuk mengetahui apa itu file FBX dan API yang dapat membuat dan membukanya.",
  "title" :"FBX - Format Berkas FilmBox 3D",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file FBX?

FBX, FilmBox, adalah format file 3D populer yang awalnya dikembangkan oleh Kaydara untuk MotionBuilder. Itu diakuisisi oleh Autodesk Inc pada tahun 2006 dan sekarang menjadi salah satu format pertukaran 3D utama seperti yang digunakan oleh banyak alat 3D. FBX tersedia dalam format file biner dan ASCII. Format ini dibuat untuk menyediakan interoperabilitas antara aplikasi pembuatan konten digital. Ada banyak alat yang tersedia untuk konversi dari/ke format file FBX.

## Format File FBX - Informasi Lebih Lanjut

FBX adalah format berpemilik dan spesifikasi tentang format file binernya tidak tersedia secara resmi. C++ FBX SDK disediakan oleh Autodesk untuk membaca, menulis, dan mengonversi ke/dari file FBX. Skrip impor dan ekspor Python untuk FBX juga tersedia di perangkat lunak Blender yang tidak menggunakan FBX SDK.

### Struktur Berkas Berbasis Teks

Struktur file berbasis teks adalah struktur pohon yang didokumentasikan dengan pengidentifikasi yang diberi nama dengan jelas. Ini terdiri dari daftar node bersarang yang diatur dalam hierarki di mana setiap node memiliki:

* Pengidentifikasi NodeType (nama kelas)
* Tuple properti yang terkait dengannya, elemen tuple adalah tipe data primitif yang biasa: ##float, integer, string## dll.
* Daftar yang berisi node dalam format yang sama (secara rekursif).

Ini dapat direpresentasikan secara logis sebagai berikut:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Beberapa node standar didefinisikan sebagai daftar implisit di mana setiap item terdiri dari daftar bersarang. Aplikasi apa pun, yang ingin mengakses geometri FBX, harus mengurai konten ini dan memanfaatkannya. Contoh file FBX berbasis teks adalah seperti yang diberikan di bawah ini:

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## Struktur File Biner dari File FBX

Seperti yang dinyatakan sebelumnya, spesifikasi format file FBX tidak tersedia untuk umum untuk FBX. Karena Blender Foundation mengimplementasikan format file FBX tanpa menggunakan SDK yang disediakan perusahaan, beberapa detail tentang format file biner [tersedia](https://code.blender.org/2013/08/fbx-binary-file-format -spesifikasi/) sebagai bagian dari implementasinya.

Struktur file biner mengikuti urutan berikut:

* Tajuk
* Rekam Objek
* Footer

### Tajuk FBX

Informasi header file terdiri dari 27 byte.

* Byte 0 - 20: Kaydara FBX Binary \x00 (file-magic, dengan 2 spasi di akhir, lalu terminator NULL).
* Byte 21 - 22: [0x1A, 0x00]## (tidak diketahui tetapi semua file yang diamati menunjukkan byte ini).
* Byte 23 - 26: unsigned int, nomor versi. 7300 untuk versi 7.3 misalnya.

### Rekam Objek ###

Header diikuti oleh rekaman objek yang merupakan rekaman simpul penuh dengan nama kosong dan daftar properti kosong. Ini secara rekursif berisi seluruh formasi file.

### Kaki ###

Bagian FBX Footer terletak di akhir file yang isinya tidak diketahui.

## Format Rekam ##

Catatan dalam file FBX dikategorikan sebagai:

* Catatan Node
* Catatan Properti

### Format Rekaman Node ###

Setiap Node Record Format diberi nama dan memiliki tata letak memori berikut.


|Ukuran (Bytes)|Jenis Tanggal|Nama
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperti
|4|UInt32|PropertiListLen
|1|UInt8|NameLen
|PanjangNama|karakter|Nama
|?|?|Properti[n], di mana n = 0:PropertiListLen
|Opsional| |
|?|?|Daftar Bersarang
|13|uint8[]|Null-Record

di mana:

* `EndOffset` adalah jarak dari awal file ke akhir record node (yakni byte pertama dari apa pun yang muncul berikutnya). Ini dapat digunakan untuk dengan mudah melewati catatan yang tidak diketahui atau tidak diperlukan.
* `NumProperties` adalah jumlah properti dalam tuple nilai yang terkait dengan node. Daftar bersarang sebagai elemen terakhir tidak dihitung sebagai properti.
* `PropertyListLen` adalah panjang daftar properti. Ini adalah ukuran yang diperlukan untuk menyimpan properti ##NumProperties##, yang bergantung pada tipe data properti.
* `NameLen` adalah panjang nama objek, dalam karakter. Satu-satunya kasus di mana ini adalah 0 tampaknya menjadi daftar tingkat atas.
* `Nama` adalah nama objek. Tidak ada terminasi nol.
* `Properti[n]` adalah properti ke-n. Untuk formatnya, lihat bagian Property Record Format. Properti ditulis secara berurutan dan tanpa padding.
* `NestedList` adalah daftar bersarang, yang kehadirannya ditandai dengan catatan NULL di bagian paling akhir.

Keberadaan entri daftar bersarang dapat ditentukan dengan memeriksa apakah masih ada byte yang tersisa hingga EndOffset tercapai. Jika demikian, rekaman objek selanjutnya harus dibaca langsung mengikuti properti terakhir. Rekaman objek kemudian mengikuti 13 byte nol, yang kemudian digabungkan dengan EndOffset. Tujuan atau persyaratan entri NULL tidak diketahui dan mungkin menunjukkan beberapa fitur format.

### Format Catatan Properti ###

Catatan properti berisi detail tentang properti yang merupakan bagian dari Node. Rekaman properti memiliki tata letak memori berikut:


|Ukuran (Byte)|Tipe Data|Nama
--- | --- | ---
|1|char|TypeCode
|?|?|Data

TypeCode mewakili kode karakter yang dipesan dalam grup yang membutuhkan penanganan serupa. TypeCodes dapat dikategorikan dalam tipe-tipe berikut dan TypeCode dapat menjadi salah satu kode karakter di antara tipe-tipe ini.

#### Jenis Primitif ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Data dalam rekaman tipe skalar primitif persis merupakan representasi biner dari nilai, dalam urutan byte little-endian.

#### Jenis Larik ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Data untuk Tipe Array lebih kompleks dan berada dalam struktur berikut.


|Ukuran (Byte)|Tipe Data|Nama
--- | --- | ---
|4|Uint32|Panjang Larik
|4|Uint32|Pengkodean
|4|Uint32|Panjang Terkompresi
|?|?|Isi

### Jenis Khusus ###

Berikut ini adalah TypeCodes Jenis Khusus.

```
S: String
R: raw binary data
```

Kedua TypeCodes ini direpresentasikan sebagai berikut:


|Ukuran (Byte)|Tipe Data|Nama
--- | --- | ---
|4|Uin32|Panjang
|Panjang| |

String tidak diakhiri dengan nol, dan mungkin berisi \0 karakter (ini sebenarnya digunakan di beberapa properti FBX).

## Referensi ##

* [FBX - SDK Autodesk](http://help.autodesk.com/view/FBX/2017/ENU/?guid#__files_GUID_105ED19A_9A5A_425E_BFD7_C1BBADA67AAB_htm)
* [Spesifikasi Format File Biner FBX](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)

