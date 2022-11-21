---
date: 2022-03-20
keywords: mxl, format file Musepack, ekstensi .mxl
pengarang:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Pelajari tentang format file MXL dan API yang dapat membuat dan membuka file MXL."
title: Format File MXL - File MusicXML Terkompresi
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Apa itu file MXL?

File MXL adalah bentuk terkompresi dari format file MusicXML yang merupakan format standar terbuka untuk pertukaran lembaran musik digital. File MusicXML teks biasa berukuran besar dan penggunaan file seperti format distribusi lembar terpengaruh dengan ukuran file yang besar. Masalah ini ditangani dengan [MusicXML](https://www.musicxml.com/) 2.0 dengan memperkenalkan format file MXL yang memampatkan file cukup untuk mengurangi ukuran file yang serupa dengan file MIDI asli. Jenis media yang disarankan untuk file MXL adalah application/vnd.recordare.musicxml.

## Berformat MXL

File MXL disimpan sebagai file [ZIP](/id/compression/zip/) terkompresi [XML](/id/web/xml/) dengan ekstensi file .mxl. File MXL dikompresi dengan algoritme DEFLATE sebagaimana ditentukan dalam [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### Struktur Berkas MXL

Setiap file MXL memiliki format XML berbasis ZIP yang harus memiliki file META-INF/container.xml yang menjelaskan titik awal versi file MusicXML. Tidak ada file .xsd terkait yang ditentukan untuk format file MXL.

File container.xml sederhana memiliki konten sebagai berikut. Contoh ini diambil dari file Dichterliebe01.mxl yang tersedia di situs web MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
Dalam contoh ini,<container> elemen adalah elemen dokumen. Itu<rootfiles> elemen dapat berisi satu atau lebih<rootfile> elemen, dengan yang pertama<rootfile> elemen yang menjelaskan root MusicXML. File MusicXML digunakan sebagai<rootfile> mungkin<score-partwise> ,<score-timewise> , atau<opus> sebagai elemen dokumennya.

## Referensi

* [File MXL Terkompresi](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

