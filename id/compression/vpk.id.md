{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File VPK - Format File Paket Aplikasi PlayStation Vita",
  "description":"Pelajari tentang format file VPK dan API yang dapat membuat dan membuka file VPK.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## Apa itu file VPK?

File dengan ekstensi .vpk adalah file paket arsip terkompresi yang digunakan untuk menginstal aplikasi pihak ketiga di konsol game Sony PlayStation Vita. File-file ini hanya dapat diinstal di jailbreak Vita PlayStation oleh HENkaku yang memungkinkan PS Vita dan PSTV untuk menggunakan konten buatan pengguna yang disesuaikan. File arsip VPK berisi semua konten yang menyusun game termasuk gambar seperti file [PNG](/id/image/png/), file pengaturan seperti [.bin](/id/disc-and-media/bin/), dan konfigurasi apa pun dalam format file [XML](/id/web/xml/).

## Format File VPK

File VPK disimpan ke disk sebagai arsip [ZIP](/id/compression/zip/) terkompresi standar. Ini mungkin berisi banyak folder dan file terkait lainnya untuk aplikasi pihak ketiga yang akan diinstal di Vita Gaming Console. Untuk melihat konten file paket VPK, ganti nama ekstensinya dari .vpu menjadi .zip, dan ekstrak konten menggunakan utilitas dekompresi standar seperti WinZip atau WinRAR.

Valvesoftware memiliki informasi mendetail tentang [format file VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format) yang dapat dirujuk dari perspektif developer.

## Bagaimana cara menginstal file VPK?

File VPK dapat diinstal dari utilitas baris perintah VPK.exe. Di OS Windows, file dapat diletakkan di file vpk.exe yang mengembalikan \*.vpk yang berisi semua file paket. Atau, alat baris perintah dapat digunakan sebagai berikut.

### Buat VPK dan Tambahkan File

```
vpk <dirname>
```

### Ekstrak File VPK

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## Penampil VPK

* [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## Referensi

* [Format File VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [File VPK](https://developer.valvesoftware.com/wiki/VPK)

