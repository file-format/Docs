{
  "date" : "2021-04-08",
  "keywords" :[ "file dayung", "format file dayung", "apa itu file dayung", "file", "contoh dayung", "ekstensi file dayung", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - Format File Arsip OpenSimulator",
  "description":"Pelajari tentang format file OAR dan API yang dapat membuat dan membuka file OAR.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Apa itu file OAR?

File dengan ekstensi .oar adalah file arsip yang digunakan oleh aplikasi OpenSimulator yang merupakan server aplikasi 3D sumber terbuka untuk membuat lingkungan virtual yang dapat diakses oleh banyak pengguna melalui jaringan. Format file OAR menyediakan data aset yang diperlukan untuk memuat sepenuhnya medan, tekstur objek, dan inventaris pada sistem yang berbeda. OpenSimulator juga memiliki hypergrid opsional yang memungkinkan pengguna mengunjungi instalasi OpenSimulator lain di seluruh web. File OAR memiliki aplikasi/dayung jenis MIME internet dan berisi satu atau lebih file yang diarsipkan.


## Format File OA

OAR adalah file biner yang disimpan dalam format file arsip terkompresi. Versi terbaru format file OAR adalah [versi 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) yang memiliki perubahan besar dari sebelumnya [versi 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). Versi terbaru mendukung penyimpanan banyak wilayah dalam satu OAR dan tidak kompatibel dengan versi OpenSimulator sebelum 0.7.5. File OAR adalah file tar yang di-gzip (tar.gz) dalam format tar unix asli (bukan USTAR).

## Contoh Wilayah OAR
File AOR dapat berisi banyak wilayah. Struktur arsip adalah sebagai berikut (contoh ini berisi 4 wilayah):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## Arsip OAR.xml

File kontrol arsip berisi nomor versi utama untuk menentukan kompatibilitas dengan perubahan format di masa mendatang. Kehadiran aset dalam format OAR ditunjukkan oleh elemen boolean<assets_included> . Informasi tentang wilayah yang disertakan dimuat dalam manifes yang ada di file kontrol. Contoh Archive.xml adalah sebagai berikut.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## Referensi

* [Format OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

