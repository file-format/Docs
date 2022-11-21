{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Format Pertukaran Bahan",
  "keywords" :[ "MXF", "matroska video", "format mkv", "cara memutar file MXF", "SMPTE", "multimedia", "video" ],
  "description":"Pelajari tentang format file MXF dan API yang dapat membuat dan membuka file MXF.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## Apa itu File MXF?

File dengan ekstensi .mxf adalah format wadah multimedia yang berisi media video dan audio digital beserta informasi metadata tentang file tersebut. Ini mengikuti standar SMPTE (Society of Motion Picture and Television Engineers) yang merupakan asosiasi global para profesional dari bidang teknik, teknologi, dan eksekutif yang bekerja di industri media dan hiburan. File MXF dapat dikonversi ke format file lain seperti [AVI](/id/video/avi/) atau [MOV](/id/video/mov/).

## Format File MXF

File MXF sebenarnya adalah file biner yang terdiri dari urutan byte dalam format tertentu. Aplikasi decoding harus sesuai dengan format ini untuk memahaminya dan mengekstrak informasi darinya. Formatnya memungkinkan penambahan item baru tanpa merusak kompatibilitas mundur menggunakan pengkodean KLV yang dijelaskan di bawah ini.

* Kunci – pengidentifikasi elemen, Label Universal SMPTE (UL)
* Panjang – panjang data yang merupakan pengkodean panjang variabel yang digunakan untuk mengurangi jumlah ruang yang diperlukan untuk item ini
* Nilai – nilai sebenarnya dari elemen.

### Spesifikasi Format SMPTE

Format file MXF telah ditentukan oleh spesifikasi SMPTE berikut.

* SMP ST 377-1:2011. Televisi — Material Exchange Format (MXF) — Spesifikasi Format File
* SMPTE ST 377-2 (sedang dalam proses per Januari 2012). Sintaks Ekstensi Berkode KLV untuk MXF.
* SMPTE ST 378:2004 (Diarsipkan 2010). Televisi — Material Exchange Format (MXF) — Pola Operasional 1a (Single Item, Single Package)
* SMPT ST 379-1:2009. Format Pertukaran Bahan (MXF) — Wadah Generik MXF
* SMPT ST 379-2:2010. Material Exchange Format (MXF) -- Penampung Generik Terbatas MXF
* SMPT ST 380:2004. Televisi — Format Pertukaran Material (MXF) — Skema Metadata Deskriptif-1 (Standar, Dinamis)
* SMPT ST 381-1:2005. Televisi — Format Pertukaran Material (MXF) — Memetakan Stream MPEG ke Wadah Generik MXF (Dinamis)
* SMPT ST 381-2:2011. Material Exchange Format (MXF) — Memetakan Aliran MPEG ke Wadah Generik Terbatas MXF
* SMPT ST 382:2007. Material Exchange Format (MXF) — Memetakan AES3 Streams dan Broadcast Wave Audio ke MXF Generic Container
* SMPT ST 383:2008. Televisi — Format Pertukaran Material (MXF) — Memetakan Data DV-DIF ke Wadah Generik MXF
* SMPT ST 384:2005. Televisi — Format Pertukaran Bahan (MXF) — Pemetaan Gambar Tidak Terkompresi ke dalam Penampung Generik MXF
* SMPT ST 385:2004. Televisi — Format Pertukaran Material (MXF) — Memetakan SDTI-CP Essence dan Metadata ke Wadah Generik MXF
* SMPTE ST 386:2004 (Diarsipkan 2010). Televisi — Format Pertukaran Material (MXF) — Memetakan Data Esensi Tipe D-10 ke Kontainer Generik MXF
* SMPTE ST 387:2004 (Diarsipkan 2010). Televisi — Format Pertukaran Material (MXF) — Memetakan Data Esensi Tipe D-11 ke Kontainer Generik MXF
* SMPTE ST 388:2004 (Diarsipkan 2010). Televisi — Format Pertukaran Material (MXF) — Memetakan Audio Berkode A-law ke dalam Kontainer Generik MXF
* SMPT ST 389:2005. Televisi — Format Pertukaran Material (MXF) — Elemen Sistem Pemutaran Terbalik Kontainer Generik MXF
* SMPT ST 390:2011. Televisi — Format Pertukaran Material (MXF) — Pola Operasional Khusus "Atom" (Representasi Sederhana dari Satu Item)
* SMPTE ST 391:2004 (Diarsipkan 2010). Televisi — Format Pertukaran Material (MXF) — Pola Operasional 1b (Item Tunggal, Paket Berkelompok)
* SMPT ST 392:2004. Televisi — Format Pertukaran Material (MXF) — Pola Operasional 2a (Item Daftar Putar, Paket Tunggal)
* SMPT ST 393:2004. Televisi — Format Pertukaran Material (MXF) — Pola Operasional 2b (Item Daftar Putar, Paket yang Dikumpulkan)
* SMPT ST 394:2006. Televisi — Format Pertukaran Material (MXF) — Skema Sistem 1 untuk Kontainer Generik MXF
* SMPST ST 405:2006. Televisi — Format Pertukaran Material (MXF) — Elemen dan Item Data Individual untuk Skema Sistem Kontainer Generik MXF 1
* SMPT ST 407:2006. Televisi — MXF — Pola Operasional 3a dan 3b
* SMPT ST 408:2006. Televisi — MXF — Pola Operasional 1c, 2c, dan 3c
* SMPTE ST 410: 2008. Format Pertukaran Material - Partisi Aliran Generik.
* SMPST ST 422:2006. Format Pertukaran Material — Memetakan JPEG2000 Codestreams ke dalam MXF Generic Container
* SMPTE ST 429.4:2006. Kemasan D-Cinema — Aplikasi MXF JPEG 2000
* SMPTE ST 429.5:2006. Pengemasan D-Cinema — File Trek Teks Berwaktu
* SMPTE ST 429.6:2006. D-Cinema Packaging — MXF Track File Essence Encryption
* SMPT ST 434:2006. Format Pertukaran Bahan — Pengodean XML untuk Metadata dan Informasi Struktur File
* SMPT ST 436:2006. Televisi — Pemetaan MXF untuk Jalur VBI dan Paket Data Tambahan
* SMPTE ST 2019-4:2009. Memetakan Unit Pengkodean VC-3 ke Wadah Generik MXF
* SMPTE ST 2037:2009. Memetakan VC-1 ke dalam Kontainer Generik MXF
* SMPTE RP 2008:2008. Format Pertukaran Material — Memetakan Aliran AVC ke Wadah Generik MXF
* SMPTE RP 2057:2011. Kereta Metadata Berbasis Teks di MXF
* SMPTE EG 41:2004. Format Pertukaran Material (MXF) — Panduan Rekayasa. Catatan: Dokumen ini tidak lagi terdaftar di situs Web SMPTE saat dikonsultasikan pada Januari 2012.
* SMPTE EG 42:2004. Format Pertukaran Bahan (MXF) — Metadata Deskriptif MXF
* SMPTE RDD 3:2008. Spesifikasi Interoperabilitas MXF e-VTR
* SMPTE RDD 9-2009. Spesifikasi Interoperabilitas MXF Produk Sony MPEG Long GOP
* Menu spreadsheet registri metadata SMPTE.

### Metadata Struktural MXF

Metadata struktural sangat penting dalam file MXF karena berisi informasi berguna tentang konten file. Metadata MXF berisi informasi seperti frekuensi gambar, ukuran bingkai, tanggal pembuatan file, dan tanggal modifikasi khusus. Metadata struktural menjelaskan struktur dan kemampuan file MXF yang mencakup penjelasan teknis berbagai komponen penting dan menyampaikan bagaimana garis waktu keluaran disusun.

## Referensi

* [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - Laporan Kemajuan](http://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [OpenSource C++ Library untuk MXF](http://www.freemxf.org/)

