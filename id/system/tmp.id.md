{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "ekstensi", "file", "format", "sistem", "file TMP", "dokumen TMP", "file TMP", "File sementara", "aplikasi", "program" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - Format Berkas Sementara",
  "description":"Pelajari tentang format file TMP dan API yang dapat membuat dan membuka file TMP.",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Apa itu file TMP? ##

File TMP mengacu pada cadangan sementara, penyimpanan, atau sistem file lain yang dihasilkan oleh program perangkat lunak. Itu kadang-kadang dibuat sebagai file yang tidak terlihat dan sering dihancurkan ketika program ditutup. File TMP juga dapat digunakan untuk menyimpan informasi sementara saat file baru sedang dibangun.

## Format File TMP ##

File TMP biasanya terdiri dari data mentah yang digunakan sebagai fase dalam proses konversi materi dari satu gaya ke gaya lainnya. Microsoft Word dan Apple Safari adalah dua aplikasi yang dapat menghasilkan dan menggunakan format file TMP.

Dokumen TMP yang dihasilkan seharusnya, secara teori, dihapus secara otomatis saat program ditutup atau mesin dimatikan. Dalam praktiknya, ini tidak selalu terjadi. Akibatnya, saat menelusuri dokumen program Anda, Anda mungkin menemukan file sementara yang tidak digunakan secara aktif oleh sistem atau perangkat lunak lainnya.

### Memori tambahan ###

Memori virtual digunakan dalam sistem operasi, namun, program yang menggunakan informasi dalam jumlah besar mungkin perlu membuat dokumen sementara.

### Komunikasi antar proses ###

Sebagian besar sistem operasi menyediakan primitif untuk mengirimkan data antar program, seperti pipa, soket, atau memori utama, tetapi metode paling sederhana adalah mentransfer file ke file sementara dan memberi tahu aplikasi penerima tentang lokasi file sementara.


## Spesifikasi Teknis ##

Memperoleh nama dokumen sementara yang khas biasanya disediakan oleh sistem operasi dan program perangkat lunak.
File sementara dapat dibuat dengan aman pada sistem POSIX menggunakan fungsi pustaka mkstemp atau tmpfile. Beberapa sistem menyertakan aplikasi mktemp POSIX (sejak hilang) sebelumnya. File-file ini biasanya ditemukan di direktori sementara reguler pada platform Unix di /TMP, atau %TEMP% (khusus untuk log-in) di mesin Windows.

Saat program berhenti atau dokumen ditutup, file sementara yang dibuat dengan tmpfile dihapus secara otomatis. GetTempFileName (Windows) atau tmpnam (POSIX) dapat digunakan untuk membuat nama file sementara yang akan bertahan lebih lama dari program yang membuatnya.

## Referensi ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
