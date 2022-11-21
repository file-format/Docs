{
  "date" : "2022-04-01",
  "keywords" :[ "file nkit", "format file nkit", "apa itu file nkit", "file", "contoh nkit", "ekstensi file nkit", "ekstensi", "format", "footer nkit", "file format nkit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Pelajari tentang format file NKIT dan API yang dapat membuat dan membuka file NKIT.",
  "title" :"NKIT - Format File Gambar Disk",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## Apa itu file NKIT?

File NKIT adalah gambar disk dari data yang diekstrak dari game NintendoWii dan GameCube. NKIT adalah untuk format Nintendo Toolkit. File kompresi [ISO](/id/compression/iso/) yang dihasilkan menggunakan data utama game ini untuk dijalankan dengan program emulator seperti Dolphin, Swiss, dan Nintendont. NKit hadir dalam format file mentah (iso) dan terkompresi (gcz) yang keduanya dirancang dengan tetap memperhatikan pemutaran dan ukuran tampilan.

## Format File NKIT

Format file NKit adalah format non-lossy dan digunakan untuk mengecilkan dan memulihkan gambar Nintendo Wii dan GameCube. Format tersedia dalam format file ISO dan GCZ untuk setiap game GameCube dan Wii.

|Sistem |Format |Perangkat Keras Didukung |Dolphin Didukung |Restorable 1:1 |Catatan|
---|---|---|---|---|---|
|GameCube| nkit.iso| Ya |Ya| Ya |Sama seperti GameCube iso yang dipadatkan|
|GameCube| nkit.gcz| Tidak| Ya| Ya |GCZ adalah format kompresi block seekable milik Dolphin sendiri|
|Wii| nkit.iso| Tidak Ya| Ya| Format RVT-H hanya dapat diputar di Dolphin|
|Wii| nkit.gcz| Tidak Ya| Ya| RVT-H di GCZ hanya dapat dimainkan di Dolphin|

### Tajuk NKIT

Header format file NKIT adalah sebagai berikut.

|Offset |Panjang |Nama|
---|---|---|
|0x200 |0x4 |NKit Tajuk 'NKIT'|
|0x204 |0x4 |NKit Versi ' v01'|
|0x208 |0x4 |Sumber gambar asli CRC32|
|0x20C |0x4 |NKit CRC - menjadikan file NKit CRC32 sama dengan CRC sumber pada 0x208 (pada 0x4 dalam GCZ)|
|0x210 |0x4 |Panjang gambar sumber|
|0x214 |0x4 |Forced Junk ID (Ketika Disc ID berbeda - jarang - GameCube saja)|
|0x218 |0x4 |Wii Perbarui partisi CRC32 jika dihapus saat mengonversi|

## Referensi ##

* [Format File NKIT - oleh gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

