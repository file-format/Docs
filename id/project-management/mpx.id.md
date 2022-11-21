{
  "date" : "2019-10-11",
  "keywords" :[ "file mpx", "format file mpx", "apa itu file mpx", "file", "contoh mpx", "ekstensi file mpx", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - Format File Pertukaran Proyek Microsoft",
  "description":"Pelajari tentang format file MPX dan API yang dapat membuat dan membuka file MPX.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Apa itu file MPX? ##

File dengan ekstensi .mpx adalah Format File Microsoft Exchange. Format file MPX dikembangkan oleh Microsoft Project (MSP) untuk memfasilitasi pertukaran informasi proyek antara MSP dan aplikasi lain yang mendukung format file MPX, termasuk Primavera Project Planner, Sciforma, dan Timerline Precision Estimating. Dengan menggunakan file MPX, Anda dapat mentransfer semua jenis informasi dari proyek ke sistem yang berbeda, seperti informasi penugasan sumber daya terperinci, informasi kalender, atau info dari kotak dialog Info Proyek.

Microsoft Project 4.0 memperkenalkan dukungan untuk membuat dan membaca format file MPX yang terus digunakan melalui Microsoft Project 98. Namun, dukungan untuk membuat file MPX telah menghentikan rilis Microsoft Project 2000, dan versi hingga Microsoft Project 2010 hanya mendukung pembacaan MPX. Format file MPX tidak didukung dalam versi setelah MSP 2010.

## Format File MPX ##

Ikhtisar spesifikasi file MPX diberikan di bagian ini. Spesifikasi lengkap dapat ditemukan di [Basis Pengetahuan](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) ini artikel dan dapat dirujuk untuk rincian.

### Catatan ###

Catatan file MPX berisi informasi untuk proyek. Ada berbagai jenis record dimana setiap record memiliki urutannya masing-masing. Setiap jenis record diidentifikasi dengan nomor recordnya. Untuk file MPX, perlu berisi jenis rekaman File Creation. Jenis catatan lain tidak wajib. Tabel berikut memperlihatkan semua tipe rekaman, nomor rekamannya, dan jumlah rekaman yang dapat dimuat setiap jenis dalam file MPX. Rekam penyertaan dalam file MPX harus mengikuti urutan tabel, dengan komentar disisipkan di mana saja.

|Nama Rekam|Nomor Rekam|Jumlah maksimum Rekam
---|---|---|
|Pembuatan File (wajib)|tidak ada|1
|Pengaturan Mata Uang|10|1
|Pengaturan Bawaan|11|1
|Pengaturan Tanggal dan Waktu|12|1
|Definisi Kalender Dasar|20|250
|Jam Kalender Dasar|25| 7 per catatan Definisi Kalender Dasar
|Pengecualian Kalender Dasar|26| 250 per catatan Definisi Kalender Dasar
|Tajuk Proyek|30|1
|Definisi Tabel Sumber Daya Teks|140|1- (Atau Anda dapat menggunakan catatan Definisi Tabel Sumber Daya Numerik)
|Definisi Tabel Sumber Daya Numerik|41|1
|Sumberdaya|50|9.999
|Catatan Sumber Daya|51| 1 per catatan Sumber Daya
|Definisi Kalender Sumber Daya|55| 1 per catatan Sumber Daya
|Jam Kalender Sumber Daya|56| 7 per Kalender Sumber Daya
|Pengecualian Kalender Sumber Daya| 57|250 per Kalender Sumber Daya
|Definisi Tabel Tugas Teks|60|1 (Atau Anda dapat menggunakan catatan Definisi Tabel Tugas Numerik)
|Definisi Tabel Tugas Numerik|61|1
|Tugas|70|9
|Catatan Tugas|71| 1 per catatan Tugas
|Tugas Berulang|72| 1 per catatan Tugas
|Penugasan Sumber Daya|75| 100 per catatan Tugas
|Bidang Kelompok Kerja Penugasan|76| 1 per catatan Penugasan
|Nama Proyek|80|500
|Tautan Klien DDE dan OLE|81|500
|Komentar|0|tidak terbatas

### Struktur Berkas ###

File MPX terdiri dari catatan yang disebutkan di atas yang disusun dengan cara yang telah ditentukan sebelumnya di dalam file. Rincian tentang jenis rekaman ini dibahas sebagai berikut:

**File Creation Record (FCR):** Ini adalah catatan wajib yang bertujuan untuk mengidentifikasi:

* Format file (MPX)
* Daftar karakter pemisah yang digunakan dalam file
* Program dan nomor versi yang digunakan untuk membuat file
* Nomor versi format file MPX yang digunakan dalam file
* Kode halaman yang digunakan untuk membuat file

Ini harus menjadi catatan pertama dalam file. Saat mengekspor dari Microsoft Project, karakter pemisah daftar ditentukan dalam item Pengaturan Regional di Panel Kontrol Windows. Catatan FCR mencakup bidang-bidang berikut:

* MPX diikuti segera oleh karakter pemisah daftar
* Nama / Pengenal Program
* Nomor Versi file
* Halaman Kode (850, 437, MAC, ANSI)

Misalnya, rekaman dapat berisi informasi **MPX, Microsoft Project, 3.0**, yang menentukan bahwa koma digunakan sebagai karakter pemisah daftar dalam file MPX ini. Versi format MPX yang digunakan dalam file diekspor dari Microsoft Project versi 3.0.

**Pengaturan Mata Uang** Catatan ini, memiliki nomor catatan 10, menentukan pengaturan untuk opsi mata uang di kotak dialog Opsi. Jika rekaman ini tidak disertakan, setelan saat ini di kotak dialog Opsi akan digunakan. Pemisah Ribuan dan Desimal ditentukan dalam item Pengaturan Wilayah di Panel Kontrol Windows.
Bidang yang termasuk dalam catatan ini adalah:

* Simbol Mata Uang
* Posisi Simbol (0 # setelah, 1 # sebelum, 2 # setelah dengan spasi, 3 # sebelum dengan spasi)
* Mata Uang Digit (0,1,2)
* Pemisah Ribuan
* Pemisah desimal

**Contoh:** 10,$,1,2,",",.
Contoh ini menentukan bahwa nilai mata uang menyertakan tanda dolar ($) di depannya, bahwa dua digit disertakan setelah titik desimal, koma digunakan untuk memisahkan ribuan, dan titik digunakan sebagai titik desimal. Karena karakter pemisah daftar disertakan dalam bidang Pemisah Ribuan, bidang tersebut diapit oleh tanda kutip.

**Pengaturan Default:** Catatan ini, memiliki catatan nomor 11, menentukan pengaturan untuk opsi default di kotak dialog Opsi. Jika durasi tidak ditentukan, Unit Durasi Default perlu diatur untuk perhitungan unit durasi yang benar. Jika rekaman ini tidak disertakan, setelan saat ini di kotak dialog Opsi akan digunakan.
Bidang yang termasuk dalam catatan ini adalah:

* Unit Durasi Default (0 # menit, 1 # jam, 2 # hari, 3 # minggu)
* Jenis Durasi Default (0 # tidak diperbaiki, 1 # diperbaiki)
* Unit Kerja Default (0 # menit, 1 # jam, 2 # hari, 3 # minggu)
* Jam/Hari Default
* Jam/Minggu Default
* Tarif Standar Default
* Tarif Lembur Default
* Memperbarui Status Tugas Memperbarui Status Sumber Daya (0 # no, 1 # yes)
* Membagi Tugas Dalam Proses (0 # no, 1 # yes)

**Pengaturan Tanggal dan Waktu:** Catatan ini, memiliki catatan nomor 12, tentukan pengaturan untuk opsi tanggal dan waktu di kotak dialog Opsi, dan opsi Format Tanggal Teks Batang di kotak dialog Tata Letak. Jika rekaman ini tidak disertakan, setelan saat ini di kotak dialog Opsi akan digunakan.
\\Bidang yang termasuk dalam catatan ini adalah:

* Tanggal Pesanan (0 # bulan/hari/tahun, 1 # hari/bulan/tahun, 2 # tahun/bulan/hari)
* Format Waktu (0 #12 jam, 1 #24 jam)
* Waktu Default (jumlah menit setelah tengah malam)
* Pemisah Tanggal
* Pemisah Waktu
* 0:00 hingga 11:59 Teks
* 12:00 hingga 23:59 Teks
*Format Tanggal (0 -14)*
* Format Tanggal Teks Batang (0 -194)*

**Definisi Kalender Dasar:** Catatan ini, memiliki nomor catatan 20, menentukan kalender dasar dan hari kerja dan hari tidak bekerja dalam seminggu. Pengaturan default digunakan jika tidak ada entri selama sehari. Pengaturan default adalah Senin sampai Jumat untuk hari kerja dan Sabtu dan Minggu untuk bukan hari kerja. Dalam rekaman ini, bidang Nama wajib diisi. Untuk setiap hari, entri 0 menunjukkan bahwa hari tersebut bukan hari kerja, dan entri 1 menunjukkan bahwa hari tersebut adalah hari kerja.
Bidang yang termasuk dalam catatan ini adalah:

* Nama
* Minggu
* Senin
* Selasa
* Rabu
* Kamis
* Jumat
* Sabtu

**Base Calendar Hours:** Record ini, memiliki record nomor 25, menentukan jam kerja untuk hari dalam seminggu jika berbeda dari pengaturan default. Jam kerja default adalah 08:00 hingga 12:00 dan 13:00 hingga 17:00 Setiap catatan Jam Kalender Dasar mengacu pada catatan Definisi Kalender Dasar sebelumnya. Hingga tujuh dari catatan ini dapat mengikuti setiap catatan Definisi Kalender Dasar.

* Hari dalam Seminggu (1 - 7, dimana 1 # Minggu dan 7 # Sabtu)
* Dari Waktu 1
* Ke Waktu 1
* Dari Waktu 2
* Ke Waktu 2
* Dari Waktu 3
* Ke Waktu 3

**Pengecualian Kalender Dasar:** Record ini, yang memiliki record nomor 26, menentukan pengecualian untuk hari dan jam yang ditentukan dalam dua jenis record sebelumnya. Hingga 250 catatan ini dapat mengikuti setiap catatan Definisi Kalender Dasar. Catatan-catatan ini harus terdaftar dalam urutan kronologis. Jika pengecualian adalah satu hari, Anda dapat mengosongkan bidang Sampai Tanggal. Jika tidak ada waktu yang ditunjukkan, waktu default dari 08:00 hingga 12:00 dan 13:00 hingga 17:00 akan digunakan.
Bidang yang termasuk dalam catatan ini adalah:

* Dari tanggal
* Saat ini
* Tidak bekerja/Bekerja (0 # tidak bekerja, 1 # bekerja)
* Dari Waktu 1
* Ke Waktu 1
* Dari Waktu 2
* Ke Waktu 2
* Dari Waktu 3
* Ke Waktu 3

**Project Header:** Record ini, memiliki nilai record 30, menyetel bidang proyek global, seperti tanggal mulai proyek dan tanggal selesai proyek. Bidang dalam rekaman ini sesuai dengan informasi di kotak dialog Info Proyek dan Statistik.
Bidang dan tab yang disertakan dalam rekaman ini adalah:

* Tab proyek
* Perusahaan
* Pengelola
* Kalender (Standar digunakan jika tidak ada entri)
* Tanggal Mulai (bidang ini atau bidang berikutnya dihitung untuk file yang diimpor, bergantung pada pengaturan Jadwal Dari)
* Tanggal Selesai
* Jadwal Dari (0 # mulai, 1 # selesai)
* Tanggal sekarang*
* Komentar
* Biaya
* Biaya Dasar
* Harga asli
* Kerja
* Pekerjaan Dasar
* Kerja nyata
* Kerja
* Durasi*
*Durasi Dasar*
* Durasi Aktual
* Persen Selesai
* Mulai Dasar
* Garis Dasar Selesai
* Awal Aktual
* Selesai Aktual
* Mulai Variasi
* Selesai Varians
* Subjek
* Pengarang
* Kata kunci

**Definisi Tabel Sumber Daya Teks**: Catatan ini mencantumkan bidang sumber daya, secara berurutan, yang sedang diimpor atau diekspor. Untuk file yang diimpor, nama harus cocok dengan nama bidang yang digunakan di Microsoft Project. Untuk file yang diekspor, rekaman ini berasal dari tabel Ekspor sumber daya. Catatan ini atau catatan Definisi Tabel Sumber Daya Numerik harus digunakan. Saat mengekspor dari Microsoft Project, kedua rekaman ini disertakan.

**Definisi Tabel Sumber Daya Numerik:** Dengan menggunakan angka, bukan nama, catatan ini mencantumkan bidang sumber daya, secara berurutan, yang sedang diimpor atau diekspor. Ini adalah metode alternatif untuk mengidentifikasi bidang sumber daya yang disertakan dalam setiap catatan Sumber Daya dan berguna saat menentukan file MPX yang dibuat oleh produk berbahasa asing.

**Sumber Daya:** Catatan ini berisi informasi untuk setiap sumber daya yang diimpor atau diekspor. Setiap catatan Sumber Daya menjelaskan satu sumber daya. Saat Anda mengimpor informasi, bidang yang disertakan ditentukan oleh rekaman Definisi Tabel Sumber Daya Teks atau rekaman Definisi Tabel Sumber Daya Numerik. Saat Anda mengekspor informasi, bidang yang disertakan adalah bidang yang tercantum dalam tabel Ekspor sumber daya.

**Catatan Sumber Daya:** Catatan ini berisi catatan tentang catatan Sumber Daya tepat sebelumnya. Untuk baris baru dalam catatan, karakter ASCII 127 digunakan. Jika catatan menyertakan karakter pemisah daftar, sertakan catatan dalam tanda kutip.

**Definisi Kalender Sumber Daya:** Catatan ini menentukan hari kerja untuk sumber daya yang ditentukan di catatan Sumber Daya tepat sebelumnya. Untuk file yang diimpor, jika tidak ada entri untuk bidang Nama Kalender Dasar, Standar akan digunakan. Tidak ada entri untuk hari tertentu yang menunjukkan bahwa hari tersebut disetel ke default (2). Jika tidak ada rekaman Definisi Kalender Sumber Daya, Standar digunakan sebagai kalender dasar untuk sumber daya, dengan default digunakan untuk hari. Untuk setiap hari, entri 0 menunjukkan bahwa hari tersebut bukan hari kerja, 1 menunjukkan bahwa hari tersebut adalah hari kerja, dan 2 menunjukkan bahwa default digunakan.

**Jam Kalender Sumber Daya:** Catatan ini menentukan jam kerja untuk sumber daya yang berbeda dari kalender dasar yang digunakan oleh sumber daya. Rekaman ini berlaku untuk rekaman Definisi Kalender Sumber Daya tepat sebelum rekaman ini. Hingga tujuh catatan ini dapat mengikuti setiap catatan Definisi Kalender Sumber Daya.

**Pengecualian Kalender Sumber Daya:** Rekaman ini menentukan pengecualian untuk hari dan jam yang ditentukan dalam dua jenis rekaman sebelumnya. Hingga 250 catatan ini dapat mengikuti setiap catatan Definisi Kalender Sumber Daya. Catatan-catatan ini harus terdaftar dalam urutan kronologis. Jika pengecualian hanya satu hari, Anda dapat mengosongkan bidang Sampai Tanggal. Jika tidak ada waktu yang ditunjukkan, waktu default dari 08:00 sampai 12:00 dan 13:00 sampai 17:00 akan digunakan.

**Definisi Tabel Tugas Teks:** Catatan ini mencantumkan bidang tugas, secara berurutan, yang sedang diimpor atau diekspor. Untuk file yang diimpor, nama harus cocok dengan nama bidang yang digunakan di Microsoft Project. Jika file sedang diekspor, rekaman ini berasal dari tabel Ekspor tugas. Saat mengekspor dari Microsoft Project, kedua rekaman ini disertakan. Bidang yang dihitung oleh Microsoft Project, seperti Mulai Terjadwal dan Selesai Terjadwal, akan diabaikan jika diimpor. Jika Anda memiliki tanggal mulai atau selesai tugas yang tetap, gunakan bidang Jenis Batasan dan Tanggal Batasan.

**Definisi Tabel Tugas Numerik:** Dengan menggunakan angka, bukan nama, catatan ini mencantumkan bidang tugas, secara berurutan, yang sedang diimpor atau diekspor. Ini adalah metode alternatif untuk mengidentifikasi bidang tugas yang disertakan dalam setiap catatan Tugas dan berguna saat menentukan file MPX yang dibuat oleh produk berbahasa asing.

**Tugas:** Catatan ini berisi informasi untuk setiap tugas yang diimpor atau diekspor. Setiap catatan Tugas menjelaskan satu tugas. Saat Anda mengimpor informasi, bidang yang disertakan ditentukan oleh catatan Definisi Tabel Tugas Teks atau catatan Definisi Tabel Tugas Numerik. Saat Anda mengekspor informasi, bidang yang disertakan adalah bidang yang tercantum dalam tabel Ekspor tugas.

**Catatan Tugas:** Catatan ini berisi catatan tentang catatan Tugas tepat sebelumnya. Gunakan karakter ASCII 127 untuk menunjukkan baris baru di dalam catatan. Jika catatan menyertakan karakter pemisah daftar, sertakan catatan dalam tanda kutip.

**Penugasan Sumber Daya**: Catatan ini mencantumkan informasi tentang sumber daya yang ditetapkan untuk tugas yang ditentukan dalam catatan Tugas sebelumnya. Jika Anda menggabungkan file dan ingin mempertahankan informasi penetapan sumber daya, Anda harus menyertakan informasi tersebut dalam file MPX. Jika Anda menggabungkan, semua tugas yang ada pada tugas yang digabungkan akan dihapus. Jika Anda menggabungkan file berdasarkan ID Unik, sumber daya ditetapkan menggunakan ID Unik Sumber Daya, bukan ID.

**Bidang Grup Kerja Penugasan Sumber Daya:** Catatan ini mencantumkan informasi yang disimpan dengan setiap tugas untuk fitur Grup Kerja Microsoft Project 4.0 dan 4.1. Jika Anda menggunakan fitur Workgroup, Anda perlu menyertakan record ini untuk memastikan tidak ada informasi yang hilang.

**Nama Proyek:** Catatan ini mencantumkan semua nama tautan DDE yang disimpan dalam proyek.

**Tautan Klien DDE dan OLE:** Catatan ini mencantumkan tautan DDE ke dalam proyek.

**Komentar:** Rekaman ini dapat digunakan untuk menambahkan komentar ke file dan dapat muncul di posisi mana pun dalam file. Setiap rekaman Komentar harus dimulai dengan "0".

## Masalah untuk Membuka file MPX ##

Berikut adalah daftar beberapa masalah umum yang mungkin timbul dan menyebabkan kesalahan fungsi format MPX:

* Tidak adanya perangkat lunak pendukung
* File rusak
* File yang terinfeksi karena virus
* Tidak ada hak akses di sistem untuk membuka file
* Drive usang di sistem Anda
* Ekstensi file diubah namanya

## Referensi ##

* [MPX - Pangkalan Pengetahuan Microsoft](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

