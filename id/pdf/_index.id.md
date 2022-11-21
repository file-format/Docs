{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :["dasar"],
  "description":"Portable Document Format (PDF) adalah representasi standar dokumen yang tidak bergantung pada perangkat lunak, perangkat keras, dan OS. Standar PDF mencakup PDF/A, PDF/E, PDF/UA, PDF/VT, dan PDF/X.",
  "title" :"Format File PDF - Apa itu file PDF?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) adalah jenis dokumen yang dibuat oleh Adobe pada tahun 1990-an. Tujuan dari format file ini adalah untuk memperkenalkan standar representasi dokumen dan bahan referensi lainnya dalam format yang independen dari perangkat lunak aplikasi, perangkat keras maupun Sistem Operasi. Format file PDF memiliki kemampuan penuh untuk memuat informasi seperti teks, gambar, hyperlink, form-fields, multimedia, tanda tangan digital, lampiran, metadata, fitur Geospasial dan objek 3D di dalamnya yang dapat menjadi bagian dari dokumen sumber.

Dalam sebagian besar kasus, dokumen yang sudah ada diubah menjadi PDF daripada membuat PDF baru dari awal. Namun bukan berarti tidak ada perangkat lunak untuk pembuatan atau manipulasi file PDF.

**(Harus berbagi sesuatu tentang format file PDF? Anda dapat memposting temuan Anda di bagian [Berita Format File PDF](https://news.fileformat.com/t/PDF).)**

## Format File PDF - Sejarah Singkat

Garis waktu cepat tentang pembentukan file PDF dalam hal garis waktu adalah sebagai berikut:

**1993** - Adobe Systems menyediakan spesifikasi PDF secara gratis

**2008** - PDF dirilis sebagai standar terbuka pada 1 Juli 2008 dan diterbitkan oleh International Organization for Standardization sebagai **ISO 32000-1:2008**.

**2008** - Adobe menerbitkan Lisensi Paten Publik untuk hak bebas royalti format ISO 32000-1 untuk semua paten yang dimiliki oleh Adobe yang diperlukan untuk membuat, menggunakan, menjual, dan mendistribusikan implementasi yang sesuai dengan PDF.

Versi pertama PDF ditetapkan sebagai PDF 1.0 yang kemudian mengalami revisi hingga PDF 1.7. PDF 1.7, yang menjadi ISO 32000-1, menyertakan beberapa teknologi hak milik non-standar juga seperti Adobe XML Forms Architecture (XFA) dan ekstensi JavaScript untuk Acrobat. Itu pada 28 Juli 2017 ketika PDF 2.0, yang dikenal sebagai ISO 32000-2:2017 diterbitkan yang tidak menyertakan teknologi non-standar apa pun.

## Spesifikasi Format File PDF

File PDF adalah sekumpulan byte yang dapat dikelompokkan menjadi token sesuai dengan aturan sintaksis yang ditentukan oleh spesifikasi PDF. Sekali atau lebih token digabungkan untuk membentuk entitas sintaksis tingkat tinggi, terutama objek, yang merupakan nilai data dasar dari mana dokumen PDF dibuat.

### Struktur File dari File PDF

Konten file PDF disusun dalam urutan berikut di dalam file.

| Tajuk
| Tubuh
| Tabel Referensi Silang
|Trailer

#### Kepala Berkas PDF ####

Terlepas dari versi PDF, file PDF dimulai dengan header yang berisi pengidentifikasi unik untuk PDF dan versi formatnya seperti %PDF-1.x dengan rentang x dari 1-7.

#### Badan File ####

Tubuh file PDF terdiri dari urutan objek tidak langsung yang mewakili isi dokumen. Objek, seperti dijelaskan di atas, mewakili komponen dokumen seperti font, halaman, dan gambar sampel. Dimulai dengan PDF 1.5, body juga dapat berisi aliran objek, yang masing-masing berisi urutan objek tidak langsung.

#### Tabel Referensi Silang ####

Tabel referensi silang berisi informasi yang memungkinkan akses acak ke objek tidak langsung di dalam file sehingga seluruh file tidak perlu dibaca untuk menemukan objek tertentu. Tabel harus berisi entri satu baris untuk setiap objek tidak langsung, menentukan offset byte dari objek tersebut di dalam badan file. (Dimulai dengan PDF 1.5, beberapa atau semua informasi referensi silang dapat dimuat dalam aliran referensi silang.

#### Cuplikan Berkas ####

Cuplikan file PDF memungkinkan pembaca yang sesuai untuk menemukan tabel referensi silang dan objek khusus tertentu dengan cepat. Pembaca yang patuh harus membaca file PDF dari ujungnya. Baris terakhir file hanya boleh berisi penanda akhir file, %%EOF. Dua baris sebelumnya harus berisi, satu per baris dan secara berurutan, kata kunci startxref dan offset byte dalam aliran dekode dari awal file ke awal kata kunci xref di bagian referensi silang terakhir.

### Objek PDF ###

File PDF mencakup beberapa jenis objek yang berbeda dari jenis berikut

* Nilai Boolean - mewakili kondisional benar atau salah
* Bilangan - Nilai bilangan bulat dan Real
* String - berisi karakter di dalam tanda kurung
* Nama - mulai dengan maju / karakter misalnya /ASomewhatLongerName menghasilkan ASomewhatLongerName
* Array - PDF mendukung array satu dimensi. Array dengan dimensi yang lebih tinggi dapat dibangun dengan menggunakan array sebagai elemen bersarang
* Kamus - kumpulan objek sebagai pasangan kunci-nilai. Ini dapat memiliki entri nol.
* Streams - mewakili urutan byte yang panjangnya tidak terbatas juga
* Null Object - mewakili nilai null

Mungkin ada objek lain seperti komentar yang diperkenalkan dengan tanda % dan mungkin berisi karakter 8-bit.

### Objek Tidak Langsung ###

Objek apa pun dalam file PDF dapat diberi label sebagai objek tidak langsung. Objek tidak langsung diberi pengidentifikasi objek unik yang dengannya objek lain dapat merujuknya. Referensi silang untuk ini dipertahankan dalam tabel indeks dan ditandai dengan kata kunci xref yang mengikuti badan utama dan memberikan offset byte dari setiap objek tidak langsung dari awal file.

### Tata Letak PDF Linear dan Non-Linear ###

Tata letak PDF dikategorikan sebagai Llnear dan non-linear tergantung pada aplikasi target dan faktor lainnya.

Non-Linear - File PDF non-linear menggunakan lebih sedikit ruang disk dibandingkan dengan file PDF linear. Halaman PDF dari dokumen berada dalam bentuk tersebar di seluruh file PDF dan itulah mengapa file non-linier lebih lambat dibandingkan dengan file linier.

Linear PDF - Menargetkan pemirsa PDF online, file PDF Linear dibuat sedemikian rupa sehingga ditulis ke disk secara linier. Ini tidak memerlukan plugin browser untuk memuat seluruh dokumen terlebih dahulu sebelum ditampilkan.

### Ikhtisar Objek ###

Seperti disebutkan, badan PDF adalah kumpulan objek yang disebutkan di atas. PDF sebagian besar didasarkan pada PostScript tanpa fitur kontrol bahasa pemrograman seperti perintah if dan loop. Perintah yang dikeluarkan oleh kode Postscript untuk menghasilkan konten grafis dikumpulkan dan diberi token sebagai tambahan dari file, grafik, atau font apa pun yang dirujuk oleh dokumen. Semua konten ini diakumulasikan ke satu file, menghasilkan output PostScript yang tersusun.

#### Teks ####

Teks dalam PDF diwakili oleh elemen teks yang sebenarnya ditampilkan dengan mesin terbang dari font. Mesin terbang adalah bentuk grafis dan tunduk pada semua manipulasi grafis, seperti transformasi koordinat. Karena pentingnya teks dalam sebagian besar deskripsi halaman, PDF menyediakan fasilitas tingkat tinggi untuk mendeskripsikan, memilih, dan membuat mesin terbang dengan mudah dan efisien.

#### Grafik ####

Operator grafik yang digunakan dalam aliran konten PDF menjelaskan tampilan halaman yang akan direproduksi pada perangkat keluaran raster. Fasilitas tersebut ditujukan untuk aplikasi printer dan tampilan. Operator grafis membentuk enam kelompok utama:

* Operator status grafis memanipulasi struktur data yang disebut status grafis, kerangka kerja global tempat operator grafis lainnya mengeksekusi. Status grafis menyertakan matriks transformasi saat ini (CTM), yang memetakan koordinat ruang pengguna yang digunakan dalam aliran konten PDF ke dalam koordinat perangkat keluaran. Ini juga mencakup warna saat ini, jalur kliping saat ini, dan banyak parameter lain yang merupakan operan implisit dari operator pengecatan.
* Operator konstruksi jalur menentukan jalur, yang menentukan bentuk, lintasan garis, dan wilayah dari berbagai jenis. Mereka termasuk operator untuk memulai jalur baru, menambahkan segmen garis dan kurva, dan menutupnya.
* Operator pengecatan jalur mengisi jalur dengan warna, mengecat garis di sepanjang jalur, atau menggunakannya sebagai batas kliping.
* Operator pengecatan lainnya melukis objek grafis yang menggambarkan dirinya sendiri. Ini termasuk gambar sampel, bayangan yang ditentukan secara geometris, dan seluruh aliran konten yang pada gilirannya berisi rangkaian operator grafis.
* Operator teks memilih dan menampilkan mesin terbang karakter dari font (deskripsi tipografi untuk mewakili karakter teks). Karena PDF memperlakukan mesin terbang sebagai bentuk grafis umum, banyak operator teks dapat dikelompokkan dengan status grafis atau operator lukisan. Namun, struktur data dan mekanisme untuk menangani glyph dan deskripsi font cukup terspesialisasi.
* Operator konten yang ditandai mengasosiasikan informasi logika tingkat tinggi dengan objek dalam aliran konten. Informasi ini tidak memengaruhi tampilan konten yang dirender; ini berguna untuk aplikasi yang menggunakan PDF untuk pertukaran dokumen.

## Referensi ##

* [Format File PDF: Struktur Dasar](https://resources.infosecinstitute.com/pdf-file-format-basic-structure/)
* [PDF - Wikipedia](https://en.wikipedia.org/wiki/PDF)
* [Referensi PDF - Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

