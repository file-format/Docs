{
  "date" : "2021-07-28",
  "keywords" :[ "file ntf", "format file ntf", "apa itu file ntf", "file", "contoh ntf", "ekstensi file ntf", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - File Format Transfer Nasional",
  "description":"Pelajari tentang format file NTF dan API yang dapat membuat dan membuka file NTF.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## Apa itu berkas NTF?
File dengan ekstensi .ntf disebut File **National Transfer Format (NTF)**; kebanyakan digunakan oleh UK Ordnance Survey (OS); khusus untuk transfer data geospasial. Ini dikelola oleh British Standards Institution. Ini telah menjadi format transfer standar untuk data digital Ordnance Survey. Proyeksi Grid Nasional Inggris, yang merupakan jenis Transverse Mercator, menampung semua informasi georeferensi untuk file NTF.

## format file NTF
Format file NTF dimiliki oleh Ordnance Survey di Inggris; didukung oleh pustaka GDB untuk impor. Versi sekarang dari format file NTF adalah 2.0. Format file ini diperkenalkan untuk mengatasi batasan segmen vektor **PCIDSK** yang hanya memiliki satu bidang atribut per struktur, tetapi ada berbagai atribut yang dapat diekstraksi dengan data vektor. Untuk menyiasatinya, format file NTF didasari memiliki dua segmen. Setiap segmen terdiri dari vektor yang sama, tetapi dengan atribut yang berbeda. Segmen pertama file vektor NTF berisi vektor dengan nomor kode fitur sebagai atributnya. Segmen kedua berisi vektor dengan nilai sebagai atributnya.

### Koordinat sistem referensi
Pustaka GDB mewakili data raster dan vektor dengan karakteristik proyeksi TM yang sesuai:

- Garis Bujur Referensi: 49,0
- Referensi Lintang: 2.0
- Salah Timur: 400000
- Arah Salah: -100000
- Skala: 0,9996012717
- Elipsoid: Airy 1830 (E009)
Tidak ada dukungan yang tersedia untuk memperbarui, atau menulis file NTF, dan file DTM juga tidak dapat ditautkan.

### Contoh Ogrinfo
Contoh berikut menggunakan **ogrinfo** pada file NTF untuk mengambil nomor lapisan:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Referensi

* [Format Transfer Nasional Inggris Raya (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Pemetaan Web - Diilustrasikan oleh Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

