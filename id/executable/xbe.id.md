{
  "date" : "2021-08-31",
  "keywords" :[ "file xbe", "format file xbe", "apa itu file xbe", "file", "contoh xbe", "ekstensi file xbe", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file XBE dan API yang dapat membuat dan membuka file XBE.",
  "title" :"XBE - File Paket Aplikasi iOS",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## Apa itu file XBE?
File yang memiliki ekstensi .xbe adalah aplikasi yang dapat dijalankan dari disk video game Xbox. File XBE adalah file utama yang dijalankan di Sistem Xbox dan biasanya tidak dibuka di komputer, tetapi dapat dibuka di PC menggunakan program emulasi Xbox. File-file ini biasanya dibuat oleh pengembang game, dan kemudian ditandatangani oleh Microsoft. Struktur file mirip dengan file Windows PE, tetapi beberapa perubahan penting sesuai dengan pengaturan XBox diterapkan agar dapat dijalankan di XBox.

## format file XBE
File XBE terdiri dari header gambar, kumpulan header bagian, sertifikat, data penyimpanan lokal utas, kumpulan versi perpustakaan, bitmap Microsoft, dan bagian yang berisi kode dan sumber daya.

### Tajuk Gambar
Header gambar terdiri dari informasi yang menjelaskan di mana komponen lain dari executable berada di dalam file, dan bagaimana runnable harus diperlakukan dan dimuat.

### Tabel TLS
Tabel TLS terdiri dari semua informasi yang diperlukan oleh XBE untuk menyiapkan penyimpanan lokal thread dengan benar. Ini pada dasarnya unik untuk Direktori TLS yang ditemukan di file PE32, dan dapat langsung disalin dari sana. Tabel ini dapat dihilangkan, jika file XBE tidak menggunakan penyimpanan lokal utas apa pun, dan bidang masing-masing di header gambar disetel ke nol.

| mengimbangi | Ukuran | Nama | Deskripsi |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Data Mentah Mulai | Alamat absolut (yaitu bukan RVA) dari awal data variabel TLS dalam gambar program. |
| 0x0004 | 0x0004 | Data Mentah Akhir | Alamat absolut (yaitu bukan RVA) dari akhir data variabel TLS dalam gambar program. |
| 0x0008 | 0x0004 | Alamat Indeks | Alamat absolut (yakni bukan RVA) dari variabel Indeks TLS. |
| 0x000C | 0x0004 | Alamat Callback | Alamat absolut (yakni bukan RVA) dari tabel fungsi callback TLS yang diakhiri null. |
| 0x0010 | 0x0004 | Ukuran Isi Nol | Jumlah byte setelah data mentah yang harus disetel ke nol di memori. |
| 0x0014 | 0x0004 | Karakteristik | Menjelaskan keselarasan. |

### Sertifikat

Sertifikat wajib untuk setiap executable Xbox yang berisi informasi tentang judul:
 


- Waktu dan tanggal pembuatan sertifikat
- Judul ID
- Nama gelar
- ID judul alternatif
- Jenis media yang diizinkan untuk menjalankan executable (HD, DVD, CD, dll.)
- Wilayah permainan
- Peringkat permainan
- Nomor cakram
- Versi: kapan
- Data mentah kunci LAN yang digunakan untuk System Link
- Data mentah kunci tanda tangan (digunakan untuk menandatangani savegames)
- Kunci tanda tangan alternatif
- Ukuran asli sertifikat
- Nama layanan online (tidak ada di executable awal)
- Jalankan bendera keamanan waktu (tidak ada di executable awal)
 


### Jenis media yang diizinkan
Jenis media yang diizinkan oleh executable untuk dijalankan. Nilai-nilai berikut diketahui:
| Jenis media | Nilai |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### Bagian
Bagian dinyatakan oleh header bagian. Header bagian dimulai tepat setelah sertifikat dan berisi informasi di mana dalam file ada bagian yang sebenarnya. Setidaknya dua bagian selalu ada di Xbox yang dapat dieksekusi:


- .teks


- .rdata


## Referensi



* [Xbe - XBox Dapat Dijalankan](https://xboxdevwiki.net/Xbe)


