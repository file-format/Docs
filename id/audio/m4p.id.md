{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "file", "ekstensi", "format", "apa itu format file m4p", "musik", "format file m4p", "M4b vs MP3", "spesifikasi format file m4p "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file M4P dan API yang dapat membuat, mengonversi, dan membuka file M4P.",
  "title" :"Format File Buku Audio M4P - MPEG-4",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Apa itu file M4P?
File dengan ekstensi .m4p adalah file audio yang biasanya tersedia di Apple iTunes store untuk diunduh. Dengan kata lain kita dapat mengatakan bahwa M4P adalah file AAC tetapi dilindungi dari penyalinan dengan menggunakan Manajemen Hak Digital (DRM). Artinya, file M4P hanya dapat diputar di sistem atau perangkat resmi. Biasanya file M4P khusus untuk perangkat multimedia Apple. Jadi file-file ini hanya dapat diputar di Apple macbook, podcast, ponsel pintar seperti iPhone 6 atau iPhone 7.

## Format File M4P
M4P adalah singkatan dari MPEG 4 Protected (audio), dan mengkodekan audio dengan codec audio lanjutan (AAC) dan melindungi file dari penggunaan file yang tidak sah. Format file ini biasanya dianggap sebagai format file audio iTunes Music Store. Apple menggunakan sistem FairPlay Digital Rights Management (DRM) untuk melindungi file M4P. FairPlay DRM didasarkan pada teknologi yang dikembangkan oleh Veridisc. Mekanisme perlindungannya bekerja dengan mengenkripsi aliran audio AAC menggunakan enkripsi AES. Pengguna menerima kunci master yang ditugaskan ke akunnya untuk dekripsi. Format file ini diperkenalkan sebagai pengganti format file MP3, karena MP3 awalnya tidak dimaksudkan sebagai file audio, melainkan sebagai layer III dalam file video MPEG 1 atau 2.


## Spesifikasi Format File M4P

Mirip dengan [M4A](/id/audio/m4a/), file M4P juga terdiri dari potongan yang berurutan. Setiap potongan memiliki 8 byte header dan dibagi menjadi:
- Ukuran potongan 4-byte (big-endian, byte tinggi dulu)
- Jenis potongan 4-byte - salah satu tanda tangan yang telah ditentukan sebelumnya: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT", "scpt ", "ctab", "ssrc".

Mirip dengan M4A, potongan pertama di M4P akan bertipe "ftype" dan memiliki sub-tipe di offset 8. M4P ditentukan oleh sub-tipe yang harus "M4P_".

Iterasi potongan, sampai potongan jenis yang tidak diketahui terdeteksi, Ini akan membuat file M4P (MPEG-4 Audio).

## Referensi ##

* [MPEG-4 Bagian 14 - Oleh Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Contoh Pemulihan](https://www.file-recovery.com/m4a-signature-format.htm)

