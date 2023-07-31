{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File DDS- File Gambar Permukaan DirectDraw",
  "description":"Pelajari tentang format file DDS dan API yang dapat membuat dan membuka file DDS.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## Apa itu file DDS?

File DDS adalah file gambar raster yang menggunakan format wadah DirectDraw Surface (DDS). Ini menyimpan tekstur yang tidak terkompresi dan terkompresi (DXTn) dan mengimplementasikan berbagai jenis untuk menyimpan berbagai jenis data. Ini juga mendukung beberapa jenis data yang berbeda seperti tekstur lapisan tunggal, tekstur dengan mipmaps, peta kubus, peta volume dan array tekstur. Ini memungkinkan file DDS untuk menyimpan model unit tekstur video game selain foto digital dan latar belakang desktop Windows. Format file DDS dikembangkan oleh Microsoft untuk digunakan dengan DirectX SDK.

## Format File DDS

File DDS disimpan sebagai file biner dan dapat digunakan dengan DirectX SDK. Ini memanfaatkan kekuatan DirectX untuk mengembangkan aplikasi rendering real-time seperti game 3D.

### Tata Letak Berkas DDS

[Tata letak file DDS](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) telah didokumentasikan oleh Microsoft secara mendetail. File DDS biner berisi informasi berikut.

* DWORD (angka ajaib) yang berisi nilai kode empat karakter 'DDS' (0x20534444).
* Deskripsi data dalam file.

DDS_HEADER menjelaskan data dan DDS_PIXELFORMAT menjelaskan format piksel. Keduanya menggantikan struktur DDSURFACEDESC2, DDSCAPS2, dan DDPIXELFORMAT DirectDraw 7 yang sudah tidak digunakan lagi.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[Panduan pemrograman format file DDS](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) menguraikan lebih lanjut detail teknis format file ini.

## Referensi

* [DDS - Oleh Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [Manual Referensi Teknis Format File ZSoft PCX](http://qzx.com/pc-gpe/pcx.txt)

