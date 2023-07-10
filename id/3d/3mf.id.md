{
  "date" : "2019-12-09",
  "keywords" :[ "file 3mf", "format file 3mf", "apa itu file 3mf", "file", "contoh 3mf", "ekstensi file 3mf", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"Pelajari tentang format file 3MF dan API yang dapat membuka dan membuat file 3MF.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## Apa itu file 3MF?

3MF, Format Manufaktur 3D, digunakan oleh aplikasi untuk merender model objek 3D ke berbagai aplikasi, platform, layanan, dan printer lainnya. Itu dibuat untuk menghindari batasan dan masalah dalam format file 3D lainnya, seperti [STL](/id/cad/stl/), untuk bekerja dengan printer 3D versi terbaru. 3MF adalah format file yang relatif baru yang telah dikembangkan dan diterbitkan oleh konsorsium 3MF. Cukup kaya untuk mendeskripsikan model secara lengkap, menyimpan informasi internal, warna, dan karakteristik lain yang membuatnya dapat diperluas untuk mendukung inovasi baru dalam pencetakan 3D. Formatnya dapat diperluas, dapat diadopsi secara luas dan bebas dari masalah yang menimpa format file lain yang banyak digunakan.

## Sejarah Singkat Format File 3MF

Keterbatasan yang ada dalam format file deskriptif model yang tersedia, seperti STL dan lainnya, mengarahkan merek-merek terkemuka untuk berkumpul dan merumuskan format file yang lebih dapat diperluas untuk pencetakan 3D. Pertimbangan penting adalah bagaimana aplikasi harus meneruskan data model ke printer 3D. Oleh karena itu, konsorsium 3MF muncul untuk mendukung format file 3D baru yang disebut 3MF dengan tujuan membuatnya cukup dapat diperpanjang untuk memenuhi kebutuhan pencetakan 3D. Beberapa perusahaan menjadi bagian dari konsorsium ini termasuk Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP dan lain-lain. Microsoft menyumbangkan format file 3D-nya yang sedang dalam proses sebagai titik awal untuk pengembangan spesifikasi lebih lanjut kolaboratif Konsorsium 3MF.

## Format File 3MF - Informasi Lebih Lanjut

3MF adalah format data berbasis XML – XML terkompresi yang dapat dibaca manusia – yang menyertakan definisi untuk data terkait manufaktur 3D, termasuk ekstensibilitas pihak ketiga untuk data khusus. Format file 3MF dirancang dengan mempertimbangkan keterbatasan dan masalah yang dihadapi oleh format file 3D lainnya. Hal ini menyebabkan perumusan format file 3MF yaitu:

* **Lengkap:** Berisi semua informasi model, material, dan properti yang diperlukan dalam satu arsip
* **Dapat dibaca manusia:** Menggunakan struktur umum seperti OPC, [ZIP](/id/compression/zip/), dan XML untuk memudahkan pengembangan
* **Sederhana:** Spesifikasi yang singkat dan jelas, memudahkan pengembangan dan validasi dengan cepat
* **Dapat diperluas:** Memanfaatkan ruang nama XML memungkinkan ekstensi publik dan pribadi dengan tetap menjaga kompatibilitas
* **Tidak ambigu:** Pengujian kesesuaian dan bahasa yang jelas memastikan file selalu konsisten dari digital ke fisik
* **Gratis:** Akses ke dan penerapan spesifikasi 3MF adalah dan akan selalu bebas dari royalti, paten, dan lisensi

Spesifikasi untuk format file 3MF dihosting melalui [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) untuk akses publik dan pembaruan berkelanjutan. Versi yang diterbitkan saat ini adalah 1.2.3 yang menjelaskan kumpulan konvensi untuk penggunaan XML dan teknologi lain yang tersedia secara luas untuk menjelaskan konten dan tampilan dari satu atau lebih model 3D. Pengembang, yang ingin membangun sistem untuk memproses format file 3MF, dapat mengacu pada spesifikasi ini untuk tujuan implementasi.

## Spesifikasi Format File 3MF

Format file 3MF menggunakan spesifikasi Open Packaging berupa arsip ZIP untuk model fisiknya. Ini mencakup serangkaian bagian dan hubungan yang terdefinisi dengan baik yang memenuhi tujuan tertentu dalam dokumen. Ini juga membuat format mengikuti fitur paket termasuk tanda tangan digital dan thumbnail.

### Dokumen 3MF - Gambaran Umum

Dokumen khas 3MF terlihat sebagai berikut:

![3MF Document Structure](https://raw.githubusercontent.com/3MFConsortium/spec_core/master/images/figure_2-1.png "3MF Document Structure")

Muatan mencakup set lengkap suku cadang yang diperlukan untuk memproses bagian Model 3D. Semua konten yang akan digunakan untuk membuat objek yang dijelaskan dalam muatan 3D HARUS dimuat dalam Dokumen 3MF. Uraian masing-masing bagian dokumen beserta statusnya sebagai kebutuhan atau pilihan dapat dilihat pada tabel berikut.


|**Nama**|**Deskripsi**|**Sumber Hubungan**|**Diperlukan/Opsional**
--- | --- | --- | ---
|Model 3D|Berisi deskripsi satu atau lebih objek 3D untuk manufaktur.|Paket|WAJIB
|Properti Inti|Bagian OPC yang berisi berbagai properti dokumen.|Paket|OPSIONAL
|Asal Tanda Tangan Digital|Bagian OPC yang merupakan akar dari tanda tangan digital dalam paket.|Paket|OPSIONAL
|Tanda Tangan Digital|Bagian OPC yang masing-masing berisi tanda tangan digital.|Asal Tanda Tangan Digital|OPSIONAL
|Sertifikat Tanda Tangan Digital|Bagian OPC yang berisi sertifikat tanda tangan digital.|Tanda Tangan Digital|OPSIONAL
|PrintTicket|Menyediakan pengaturan untuk digunakan saat mengeluarkan objek 3D di bagian Model 3D.|Model 3D|OPSIONAL
|Thumbnail|Berisi gambar JPEG atau PNG kecil yang mewakili objek 3D di dalam paket atau paket secara keseluruhan.|Paket|OPSIONAL
|Tekstur 3D|Berisi tekstur yang digunakan untuk menerapkan warna pada objek 3D di bagian Model 3D (tersedia untuk ekstensi)|Model 3D|OPSIONAL
|Bagian Kustom|Bagian OPC yang terkait dengan metadata|Paket|OPSIONAL

[Bagian dan Hubungan](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [Model 3D](https:/ /github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Sumber Daya Objek](https://github.com/3MFConsortium/spec_core/blob/master /3MF%20Core%20Specification.md#chapter-4-object-resources), [Sumber Daya Material](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5 -material-resources) dan [Fitur Paket](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) bagian spesifikasi dokumen memberikan informasi rinci tentang dokumen 3MF.

## Referensi ##

* [Spesifikasi Format File 3MF](https://github.com/3MFConsortium/spec_core)
* [3MF - Oleh Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

