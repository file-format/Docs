{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - Format File Gambar Disk",
  "description":"Apa itu file ISO dan API yang dapat membuat dan membuka file ISO.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Apa itu file ISO?

File dengan ekstensi .iso adalah file gambar disk arsip yang tidak dikompresi yang mewakili konten seluruh data pada disk optik seperti CD atau DVD. Berdasarkan standar [ISO-9660](https://www.iso.org/standard/17505.html), format file gambar ISO berisi data disk beserta informasi sistem file yang disimpan di dalamnya. Kemampuan file ISO untuk memuat replika konten yang tepat menjadikannya jenis file yang sempurna untuk membuat salinan CD/DVD dan sebagian besar digunakan untuk menyimpan data yang dapat di-boot untuk instalasi. Sering kali, file ISO dibakar ke USB/CD/DVD sebagai konten yang dapat di-boot untuk mem-boot mesin untuk instalasi. File ISO memiliki aplikasi tipe MIME/x-iso9660-image.

## Berformat ISO

Format file ISO tidak seperti format file kontainer lainnya meskipun mengarsipkan konten data yang ditentukan. Arsip dibuat sebagai file biner dengan struktur konten dan informasi sistem file yang tepat. Format file ISO dijelaskan oleh [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) sebagai berikut.

### Struktur Tingkat Atas File ISO

Struktur keseluruhan file terdiri dari:

* `System Area` - 32.768 byte dan tidak digunakan oleh ISO_9660
* `Data Area` - terdiri dari kumpulan deskriptor Volume dan tabel Path, direktori, dan file

### Set Deskriptor Volume

Area data dimulai dengan set deskriptor volume, satu set dari satu atau lebih deskriptor volume diakhiri dengan terminator set deskriptor volume. Ini secara kolektif bertindak sebagai header untuk area data, menjelaskan kontennya (mirip dengan blok parameter BIOS yang digunakan oleh disk berformat FAT, HPFS, dan NTFS).

Set deskriptor volume seperti yang ditunjukkan di bawah ini.

|Kumpulan Deskriptor Volume|
---|
|Deskripsi volume #1|
|...|
|Deskriptor volume #N|
|Deskriptor volume menyetel terminator|

#### Deskripsi Volume

Setiap deskriptor volume berukuran 2048 byte dan memiliki struktur sebagai berikut:

|Bagian |Jenis |Identifier |Versi |Data|
---|---|---|---|---|
|Ukuran |1 byte |5 byte (selalu 'CD001') |1 byte (selalu 0x01) |2.041 byte|

## Referensi

* [Gambar Disk Optik - Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Berkas Tanda Tangan](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 - Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)

