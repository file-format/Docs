{
  "date" : "2021-07-29",
  "keywords" :[ "file shx", "format file shx", "apa itu file shx", "file", "contoh shx", "ekstensi file shx", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - Format Indeks Bentuk Shapefile",
  "description":"Pelajari tentang format file SHX dan API yang dapat membuat dan membuka file SHX.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Apa itu file SHX?
File SHX milik format indeks bentuk yang merupakan indeks posisi dari geometri fitur untuk memungkinkan mencari maju dan mundur dengan cepat. SHX adalah file offset akses langsung. Tidak ada data dalam file ini, hanya salinan duplikat dari seratus byte pertama, nomor record dan offset ke byte awal dari record tersebut di shp. Perhatikan bahwa file dengan ekstensi .shx tidak mengikat [SHP](/id/gis/shp/) dan [DBF](/id/database/dbf/).

## format file SHX
Format SHX berisi indeks posisi dari geometri fitur dan header 100-byte yang mirip dengan file SHP, diikuti oleh sejumlah record dengan panjang tetap 8-byte yang berisi dua bidang berikut:
| Byte | Ketik | Endianness | Penggunaan |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | besar | Rekam offset (dalam kata 16-bit) |
| 4–7 | int32 | besar | Rekam panjang (dalam kata 16-bit) |

Indeks ini memungkinkan untuk mencari mundur di shapefile dengan, pertama, mencari mundur di indeks bentuk dan kemudian membaca catatan offset. Offset tersebut dapat digunakan untuk mencari posisi yang benar dalam file SHP. Anda juga dapat mencari ke depan; sejumlah record yang berubah-ubah menggunakan metode yang sama. Meskipun dimungkinkan untuk menghasilkan indeks lengkap bersama dengan file SHP, tetapi ini dapat meningkatkan kemungkinan membuat file SHP rusak dengan cepat.


## Referensi

* [Shapefile - oleh Wikipedia)](https://en.wikipedia.org/wiki/Shapefile)


