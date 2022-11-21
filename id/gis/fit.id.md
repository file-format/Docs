{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File FIT- File Aktivitas Garmin",
  "description":"Pelajari tentang format file FIT dan API yang dapat membuat dan membuka file FIT.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Apa itu file FIT?

File FIT adalah file GIS yang dibuat oleh perangkat wearable olahraga Garmin. Ini digunakan untuk merekam aktivitas seseorang saat dia bergerak memakai perangkat ini. Data aktivitas mencakup lokasi dan waktu yang direkam oleh perangkat GPS. File FIT juga digunakan untuk mentransfer data aktivitas yang direkam menggunakan API web. Itulah alasan file FIT adalah format file yang paling umum digunakan untuk berbagi data kebugaran dengan platform kebugaran lainnya. Format file umum lainnya termasuk [GPX](/id/gis/gpx/), TCX, dan [KML](/id/gis/kml/).

## Format File FIT - Informasi Lebih Lanjut

File FIT disimpan ke disk sebagai file biner dengan informasi yang direkam oleh perangkat Garmin untuk aktivitas tersebut. Informasi yang disimpan di dalam file FIT meliputi:

* Tanggal Waktu
* Jenis olahraga
* Lap & pisahkan data
* Jalur GPS
* Informasi sensor
* Acara untuk sesi aktif

Data aktivitas dapat direkam dalam file secara real time atau diekspor setelah perekaman aktivitas selesai.

### Pesan Aktivitas FIT

File aktivitas FIT mungkin menyertakan beberapa jenis pesan yang diperlukan. Berikut ini adalah pesan yang diperlukan untuk file aktivitas.

|Pesan|Tujuan|
---|---|
|Id Berkas| Pesan Id File diperlukan oleh semua jenis file FIT dan diharapkan menjadi pesan pertama dalam file. Untuk file Aktivitas, properti Type harus diatur ke 4.|
|Aktivitas| Satu pesan Aktivitas diperlukan dalam file Aktivitas FIT. Termasuk dalam pesan Aktivitas adalah properti Stempel Waktu Lokal dan Jumlah Sesi. Stempel Waktu Lokal digunakan untuk menentukan offset zona waktu yang dapat diterapkan ke semua stempel waktu dalam file. Sebagian besar perangkat merekam file FIT secara real time dan jumlah sesi tidak akan diketahui hingga akhir perekaman. Oleh karena itu, pesan Aktivitas sering kali menjadi pesan terakhir dalam file.|
|Sesi| File aktivitas akan berisi satu atau beberapa pesan Sesi. Pesan Sesi adalah jenis pesan Ringkasan. Waktu Mulai, Total Waktu Berlalu, Total Waktu Pengatur Waktu, dan Stempel Waktu adalah kolom wajib diisi untuk semua pesan ringkasan.|
|Lap| Pesan putaran mewakili putaran atau interval dalam sesi. Pesan Lap adalah jenis pesan Ringkasan. Waktu Mulai, Total Waktu Berlalu, Total Waktu Pengatur Waktu, dan Stempel Waktu adalah kolom wajib diisi untuk semua pesan ringkasan.|
|Rekam| Rekam pesan termasuk koordinat GPS, kecepatan, jarak, detak jantung, daya, dll.|

## FIT File Sumber Daya Berguna

* [Mendekode File Aktivitas FIT](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [Encoding FIT Activity Files](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Referensi ##

* [File Aktivitas FIT](https://developer.garmin.com/fit/file-types/activity/)

