---
date: 2019-10-11
keywords: vob, .vob, format file vob, format file .vob, ekstensi .vob, ekstensi vob, format video vob, file vob dvd
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Pelajari tentang format file VOB dan API yang dapat membuat dan membuka file VOB."
title: Format File VOB
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Apa itu file VOB? ##

File VOB biasanya disimpan di direktori VIDEO_TS pada DVD dengan ekstensi .vob. File VOB berisi data video dan audio serta data lain seperti menu dan subtitle. VOB didasarkan pada format aliran program MPEG-2 tetapi memiliki batasan dan spesifikasi tambahan dalam aliran pribadi. File VOB adalah subset ketat dari aliran program MPEG sehingga semua file VOB adalah aliran program MPEG tetapi semua aliran program MPEG tidak sesuai dengan VOB.

## Struktur Video DVD ##

Saat DVD dibuka di komputer, VIDEO_TS adalah direktori tingkat atas dengan AUDIO_TS. AUDIO_TS kosong dan tidak digunakan. Di dalam direktori VIDEO_TS terdapat file VOB, BUP, dan IFO. File VOB berisi konten MPEG. Ini dipecah menjadi potongan berukuran 1 GB atau kurang sehingga ini kompatibel dengan semua sistem operasi. File IFO berisi informasi mengenai menu dan struktur judul. File BUK adalah file cadangan dari file IFO dengan nama yang sama. File-file ini dimaksudkan untuk disimpan di tempat terpisah secara fisik sehingga jika file IFO rusak karena kerusakan fisik pada DVD, file BUK dapat memberikan informasi yang sama.

### Tata Letak Fisik ###

- Semua file pada disk harus bersebelahan.
- File terkait harus bersebelahan (VOB, IFO, BUP).
- File bernomor harus dalam urutan menaik.

## Perlindungan Salinan ##

Banyak DVD video dienkripsi dan mencegah penyalinan data dari DVD. Kunci autentikasi dan dekripsi diperlukan untuk memutar file yang terletak di area awal DVD yang tidak dapat diakses. Kunci ini digunakan oleh perangkat lunak dekripsi CSS yang ada di pemutar DVD atau pemutar perangkat lunak. Tanpa kunci, file video tidak dapat diputar karena kunci akan diminta saat file dibuka.

## Referensi ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Di dalam DVD-Video/Struktur Direktori](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

