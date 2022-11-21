---
date: 2021-07-05
keywords: spc, .spc, format file spc, cara membuka file spc, File Sertifikat Penerbit Perangkat Lunak
pengarang:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - File Sertifikat Penerbit Perangkat Lunak
linktitle: SPC
description: "Pelajari tentang apa itu format file SPC dan API yang dapat membuat dan membuka file SPC."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Apa itu file SPC?

File dengan ekstensi .spc adalah file sertifikat keamanan digital yang dibuat dalam format PKCS #7. Beberapa aplikasi, buat file sertifikat ini untuk pertukaran informasi yang aman. Beberapa aplikasi tersebut termasuk OpenSSL dan aplikasi Signcode.exe disertakan dengan Microsoft .NET Framework. Seperti file sertifikat lainnya seperti [.cer](/id/web/cer/), [.p7c](/id/web/p7c/), dan [.ssp](/id/web/ssp/), file SPC berisi kunci publik informasi yang dienkripsi dengan kunci privat. Kunci publik ini dapat dibagikan dengan pengguna secara publik sementara kunci pribadi dirahasiakan.

## Format File SPC - Informasi Lebih Lanjut

File SPC disimpan ke disk sebagai file biner yang dapat dibuka di editor teks apa pun tetapi tidak dapat dibaca oleh manusia. Ini didasarkan pada versi terbaru PKCS #7 yang tersedia [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## Referensi

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [Referensi SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

