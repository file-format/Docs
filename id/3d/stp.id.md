---
date: 2022-01-31
keywords: stp, .stp, format file stp, cara membuka file stp, ekstensi .stp, ekstensi stp
pengarang:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format File STP
linktitle: STP
description: "Pelajari tentang format file STP dan API yang dapat membuat dan membuka file STP."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Apa itu file STP?

File STP adalah file CAD 3D yang digunakan untuk pertukaran data produk antara aplikasi CAD dan CAM. Ini berisi informasi tentang objek 3D dan disimpan mirip dengan format file **STEP**. File STP memfasilitasi pertukaran data antar aplikasi sesuai dengan [LANGKAH](/id/3d/step/) Protokol Aplikasi ISO 10303-2xx. ISO ini mendefinisikan mekanisme pengkodean untuk representasi data dalam bahasa pemodelan data EXPRESS. File STP dapat dibuka di aplikasi seperti **Autodesk Fusion 360**.

## Format Berkas STP - Informasi Lebih Lanjut

File STP disimpan ke disk dalam format file ASCII biasa. Ini berisi informasi model 3D sebagai teks biasa yang dapat dibaca oleh aplikasi CAD/CAM untuk memuat model ini.

File STP juga disimpan dengan ekstensi .step dan terdiri dari urutan catatan. Fitur yang menonjol tentang file ini meliputi:

* Kumpulan karakter didefinisikan sebagai poin kode ISO 10646.
* "ISO-10303-21;" adalah karakter pertama dalam rekaman pertama.
* Komentar dikelilingi oleh karakter "/*" dan "*/".
* Rekaman terakhir berisi "END-ISO-10303-21;" jika file LANGKAH sesuai dengan versi 2002.
* Jika sesuai dengan versi 2016, mungkin ada satu atau lebih tanda tangan digital setelah "END-ISO-10303-21;" terminator.
* Hentian baris ditandai dengan "\N\" dan jeda halaman ditandai dengan "\F\".

## Buka File STP

File STP dapat dibuka di Penampil STP serta Editor Teks.

### Buka File STP dengan STP Viewer

Berbagai aplikasi CAD dapat membuka file STP untuk dilihat di Windows, MacOS dan Linux. Ini termasuk:

* Autodesk Fusion 360 (lintas platform)
* FreeCAD (lintas platform)
* IMSI TurboCAD (Windows, Mac)
* Sistem Dassault CATIA (WIndows, Linux)

### Buka File STP dengan Editor Teks

File STP disimpan sebagai file teks biasa. Ini memungkinkan untuk membuka file STP dengan editor teks. Editor teks populer seperti Notepad dan Notepad++ di OS Windows, dan Apple TextEdit di MacOS dapat membuka file STP. Setelah dibuka di editor teks, pengguna dapat mengedit properti file STP. Namun, ini dapat menyebabkan kerusakan file jika memperbarui properti secara tidak benar.

## Cara mengonversi file STP

Ada beberapa aplikasi yang dapat mengonversi file STP ke format file lain. Aplikasi CAD yang dapat mengonversi file STP meliputi:

* Autodesk Fusion 360
*IMSITurboCAD
* Tepi Padat Siemens

Selain itu, ada beberapa aplikasi online yang dapat mengonversi file STP ke format file lain. Aplikasi online ini memungkinkan Anda mengunggah file STP Anda ke server cloud tempat file tersebut dikonversi ke format yang Anda inginkan dan dikembalikan untuk diunduh.

Autodesk Fusion 360 dapat mengonversi file STP ke format file 3D dan CAD berikut.

* [OBJ](/id/3d/obj/)
* [3MF](/id/3d/3mf/)
* [DWG](/id/cad/dwg/)
* [DXF](/id/cad/dxf/)
* [ASM](/id/cad/asm/)
* [IGES](/id/cad/iges/)
* [STL](/id/cad/stl/)
* [FBX](/id/3d/fbx/)
* F3D
* [USD](/id/3d/usd/)

## Referensi

* [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

