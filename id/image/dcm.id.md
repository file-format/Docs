{
  "date" : "2019-10-11",
  "keywords" :[ "file dcm", "format file dcm", "apa itu file dcm", "file", "contoh dcm", "ekstensi file dcm", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File DCM - File Informasi Medis Digital",
  "description":"Pelajari tentang format file DCM dan API yang dapat membuat dan membuka file DCM.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## Apa itu file DCM?

File dengan ekstensi .dcm merupakan citra digital yang menyimpan informasi medis pasien seperti MRI, CT scan, dan citra USG. File DCM menggunakan format file gambar [DICOM](/id/image/dicom) (Digital Imaging and Communications in Medicine) dan dapat menyertakan informasi pasien untuk referensi. Ini dikembangkan oleh [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) dan dimaksudkan untuk membakukan format file pencitraan untuk distribusi dan tampilan gambar medis.

## Format File DCM

File DCM menyimpan informasi dalam format gambar DICOM. File-file ini menyimpan Kumpulan Data, yang merupakan informasi dunia nyata, yang mewakili contoh SOP yang terkait dengan DICOM IOD. Informasi Meta File DICOM disimpan dalam file diikuti oleh aliran byte dari kumpulan data aktual.

### Informasi Meta File DICOM ##

Setiap file DICOM menyertakan header informasi identifikasi untuk kumpulan data yang dienkapsulasi yang terdiri dari:
* Pembukaan File 128-byte
* Awalan DICOM 4 byte
* Berkas Elemen Meta

Header ini adalah suatu keharusan untuk setiap file DICOM.

### File Meta Elemen ###
|Nama Atribut|Tag|Jenis| Deskripsi Atribut
---|---|---|---|
|Pembukaan File|Tanpa Tag atau Bidang Panjang|1|Field 128 byte tetap tersedia untuk Profil Aplikasi atau penggunaan yang ditentukan implementasi. Jika tidak digunakan oleh Profil Aplikasi atau implementasi khusus, semua byte harus diatur ke 00H. Pembaca atau Pembaharu File-set tidak akan bergantung pada konten Pembukaan ini untuk menentukan bahwa File ini adalah atau bukan File DICOM.
|DICOM Prefix|No Tag or Length Fields|1|Empat byte berisi string karakter "DICM". Awalan ini dimaksudkan untuk digunakan untuk mengenali bahwa File ini adalah atau bukan File DICOM.
|Panjang Grup Informasi Meta File|(0002,0000)|1|Jumlah byte yang mengikuti Elemen Meta File ini (akhir bidang Nilai) hingga dan termasuk Elemen Meta File terakhir dari Informasi Meta File Grup 2
|File Meta Information Version|(0002,0001)|1|Ini adalah bidang dua byte di mana setiap bit mengidentifikasi versi header File Meta Information ini. Dalam versi 1 nilai byte pertama adalah 00H dan nilai byte nilai kedua adalah 01H. Implementasi membaca File dengan Informasi Meta di mana atribut ini memiliki bit 0 (lsb) dari byte kedua yang disetel ke 1 dapat menafsirkan Informasi Meta File sebagaimana ditentukan dalam ini versi PS3.10. Semua bit lainnya tidak boleh diperiksa.
|Kelas SOP Penyimpanan Media UID|(0002,0002)|1|Secara unik mengidentifikasi Kelas SOP yang terkait dengan Kumpulan Data. UID Kelas SOP yang diizinkan untuk penyimpanan media ditentukan dalam PS3.4 - Profil Aplikasi Penyimpanan Media.
|Instans SOP Penyimpanan Media UID|(0002,0003)|1|Secara unik mengidentifikasi Instans SOP yang terkait dengan Kumpulan Data yang ditempatkan di file dan mengikuti Informasi Meta File.
|Transfer Sintaks UID|(0002,0010)|1|Secara unik mengidentifikasi Sintaks Transfer yang digunakan untuk menyandikan Kumpulan Data berikut. Sintaks Transfer ini tidak berlaku untuk Informasi Meta File.
|UID Kelas Implementasi|(0002,0012)|1|Identifikasi unik implementasi yang menulis file ini dan kontennya. Ini memberikan identifikasi yang tidak ambigu dari jenis implementasi yang terakhir menulis file jika terjadi masalah pertukaran.
|Nama Versi Implementasi|(0002,0013)|3|Mengidentifikasi versi untuk UID Kelas Implementasi (0002,0012) yang menggunakan hingga 16 karakter repertoar.
|Judul Entitas Aplikasi Sumber|(0002,0016)|3|Judul Entitas Aplikasi DICOM (AE) dari AE yang menulis konten file ini (atau terakhir memperbaruinya). Jika digunakan, ini memungkinkan penelusuran sumber kesalahan jika terjadi masalah pertukaran media.
|UID Pembuat Informasi Pribadi|(0002,0100)|3|UID pembuat informasi pribadi (0002,0102).
|Informasi Pribadi|(0002,0102)|1C|Berisi Informasi Pribadi yang ditempatkan di File Informasi Meta. Pencipta harus diidentifikasi dalam (0002,0100). Diperlukan jika UID Pencipta Informasi Pribadi (0002,0100) ada.

### Enkapsulasi Kumpulan Data ###

File DICOM berisi Kumpulan Data tunggal yang mewakili Instans SOP tunggal yang terkait dengan Kelas SOP tunggal. Transfer Syntax UID dari DICOM File Meta Information akan menentukan Transfer Syntax yang digunakan untuk mengkodekan Kumpulan Data.

### Dukungan untuk Informasi Manajemen File ###

Lapisan Format Media menyediakan Informasi Manajemen File berikut jika diperlukan untuk Profil Aplikasi DICOM tertentu.

* Identifikasi pemilik konten file

* Statistik akses file (misalnya, tanggal dan waktu pembuatan)

* Kontrol akses file aplikasi

* Kontrol akses media fisik (misalnya, proteksi tulis)

## Referensi ##
* [Standar DICOM](https://www.dicomstandard.org/current/)
* [Format File DICOM](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

