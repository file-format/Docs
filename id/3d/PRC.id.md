---
date: 2019-10-11
keywords: prc, .prc, format file prc, cara membuka file prc, ekstensi .prc, ekstensi prc
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File RRC
linktitle: PRC
description: "Pelajari tentang format file PRC dan API yang dapat membuat dan membuka file PRC."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## Format file PRC
Ekstensi ".prc" sedang digunakan untuk format file Representasi Produk 3D Ringkas dan format file e-book oleh MobiPocket.

## Apa itu file Compact Representasi Produk (PRC)?

PRC (Product Representation Compact) adalah format file 3D yang dioptimalkan untuk menyimpan, memuat, dan menampilkan data 3D terutama yang berasal dari sistem CAD (Computer-Aided Design). Ini adalah file biner berurutan, ditulis dengan cara portabel. PRC dapat digunakan untuk menyematkan data 3D dalam file PDF. PRC mendukung sebagian besar konstruksi utama CAD seperti rakitan dan bagian, pohon entitas 3D, representasi geometri eksak, representasi triangulasi, dan markup. PRC menggunakan ekstensi .prc dan jenis media internet yang digunakan adalah *model/prc*.

PRC adalah format file multiguna yang berdasarkan penggunaannya dapat disimpan menggunakan kompresi biasa untuk langsung mewakili data CAD atau disimpan menggunakan kompresi tinggi untuk memperkecil ukuran file. Data 3D yang disimpan dalam PDF menggunakan format PRC dapat dioperasikan dengan aplikasi CAM dan CAE.

### Spesifikasi Format File Ringkas Representasi Produk (RRC).

File PRC memiliki satu bagian header utama diikuti oleh satu atau lebih struktur file diikuti oleh satu file model di bagian akhir. Struktur file memiliki satu header diikuti oleh bagian data berikut:

- **Global**: Ini berisi struktur dan warna file yang direferensikan, gaya garis, dan sistem koordinat untuk setiap entitas pohon dari struktur file.
- **Pohon**: Berisi deskripsi pohon item seperti kejadian produk, definisi bagian, item representasi, dan markup.
- **Tessellation**: Ini berisi semua data tessellated (triangulasi) di entitas daun pohon (item representasi dan markup).
- **Geometri**: Berisi semua data geometri dan topologi eksak dari entitas daun pohon (item representasi).
- **Geometri Ekstra**: Berisi data ringkasan geometri. Ini memungkinkan file dimuat sebagian tanpa memuat seluruh geometri.

Berikut ini adalah struktur file PRC tipikal.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## Apa itu file e-book MobiPocket dengan ekstensi RRC
Format file e-book yang diperkenalkan oleh perusahaan Prancis bernama **Mobipocket** juga menggunakan ekstensi ".prc". Awalnya, Mobipocket meluncurkan aplikasi gratis untuk beberapa perangkat pintar seperti, komputer tablet, PDA, dan smartphone. Ekstensi ".prc" sebenarnya identik dengan .mobi tetapi digunakan khususnya untuk PDA yang hanya mendukung ekstensi **.prc** atau **.pdb**.

### Spesifikasi format file PRC Mobipocket
Format file PRC MobiPocket didasarkan pada standar Open eBook menggunakan XHTML dan juga dapat menyertakan JavaScript dan bingkai. Dukungan untuk kueri SQL asli untuk digunakan dengan database tersemat juga tersedia.

Mobipocket Reader memiliki perpustakaan halaman rumah. Pembaca dapat menyisipkan halaman kosong di bagian mana pun dari buku dan menambahkan gambar variabel. Objek seperti Anotasi, bookmark, koreksi, catatan, dan gambar dapat dikelola dari satu lokasi. Gambar dikonversi ke format GIF dan memiliki ukuran maksimal 64K yang cukup untuk ponsel dengan layar kecil. Mobipocket Reader memiliki penanda elektronik, dan kamus bawaan.

Pembaca memiliki mode layar penuh untuk membaca dan mendukung banyak PDA, Komunikator, dan Smartphone. Produk Mobipocket mendukung sebagian besar sistem operasi Palm, Windows, Symbian, BlackBerry, tetapi bukan Android. Pembaca bekerja di Linux atau Mac OS X menggunakan WINE.

## Referensi

- [RRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [Spesifikasi Format PRC](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Perbandingan format e-book - Oleh Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

