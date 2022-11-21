{
  "date" : "2021-02-15",
  "keywords" :[ "file asf", "format file asf", "apa itu file asf", "file", "contoh asf", "ekstensi file asf", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - Format File Sistem Lanjutan",
  "description":"Pelajari tentang format file ASF dan API yang dapat membuat dan membuka file ASF.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Apa itu file ASF?

File dengan ekstensi .asf adalah format file multimedia untuk menyimpan dan memutar aliran media digital melalui jaringan. Ini adalah format file kontainer yang dapat memiliki konten video dan audio untuk streaming online. Anda jarang akan menemukan file ASF, dan lebih mungkin menemukan file Windows Media Audio ([WMA](/id/audio/wma/)) dan Windows Media Video ([WMV](/id/video/wmv/)) yang keduanya menentukan file ASF memiliki konten yang dikodekan dengan codec masing-masing. File media Windows dapat dibuat dan dibaca menggunakan Windows Media Format SDK.

## Format File ASF

File ASF dapat terdiri dari beberapa aliran independen atau dependen. Ini dapat mencakup beberapa streaming audio untuk audio multisaluran atau beberapa streaming video bitrate. Beberapa bitrate membuat streaming cocok untuk transmisi melalui bandwidth yang berbeda. Selain itu, aliran dalam file ASF dapat dalam format terkompresi atau tidak terkompresi. Kompresi terbaik dicapai dengan codec Microsoft Windows Media Audio dan Video 9 Series. Spesifikasi lengkap format file ASF tersedia di [Situs Web Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### Struktur File Tingkat Atas ASF

File ASF secara logis berisi tiga jenis objek tingkat atas:

* `Header Object` - wajib dan harus ditempatkan di awal setiap file ASF
* `Data Object` - wajib dan harus mengikuti objek header
* `Index Object(s)` - opsional, tetapi berguna dalam menyediakan akses acak berbasis waktu ke dalam file ASF

Gambar berikut menunjukkan struktur file tingkat atas dari file ASF.

![ASF File Structure](../asf.png "ASF File Structure")

#### Objek Header Tingkat Atas ASF

Objek Header menyediakan urutan byte terkenal di awal file ASF dan secara opsional dapat berisi metadata seperti informasi bibliografi. Ini berisi semua informasi yang diperlukan untuk menginterpretasikan informasi dalam objek data dengan benar. Objek Header dapat mencakup beberapa objek standar termasuk, namun tidak terbatas pada:

* Objek Properti File - Berisi atribut file global.
* Stream Properties Object - Menentukan aliran media digital dan karakteristiknya.
* Objek Ekstensi Header - Memungkinkan fungsionalitas tambahan untuk ditambahkan ke file ASF sambil mempertahankan kompatibilitas ke belakang.
* Objek Deskripsi Konten - Berisi informasi bibliografi.
* Script Command Object - Berisi perintah-perintah yang dapat dijalankan pada waktu playback.
* Objek Penanda - Menyediakan titik lompatan bernama dalam file.

Objek Header direpresentasikan menggunakan struktur berikut:

|Nama bidang |Jenis bidang |Ukuran (bit)|
---|---|---|
|ID Objek| PANDUAN| 128|
|Ukuran Objek| QWORD| 64|
|Jumlah Objek Tajuk| DWORD| 32|
|Dicadangkan1| BYTE| 8|
|Dicadangkan2| BYTE| 8|

#### Objek Data Tingkat Atas ASF

Semua data media digital untuk file ASF terkandung dalam objek data dan disimpan dalam bentuk paket data ASF. Setiap paket data memiliki panjang tetap dan berisi data untuk satu atau lebih aliran media digital.

#### Objek Indeks Tingkat Atas ASF

Objek indeks tingkat atas ASF memiliki dua tipe berikut:

* `Simple Index Object` - Berisi indeks berbasis waktu dari data video dalam file ASF. Interval waktu antara entri indeks adalah konstan dan disimpan dalam Objek Indeks Sederhana.
* `Objek Indeks` - Mengacu pada Objek Indeks, Objek Indeks Objek Media, dan Objek Indeks Kode Waktu, yang formatnya serupa. Seperti Objek Indeks Sederhana, Objek Indeks mengindeks menurut waktu dengan interval waktu tetap tetapi tidak terbatas pada aliran video.

## Referensi

* [Format File ASF - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [Format File QuickTime - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

