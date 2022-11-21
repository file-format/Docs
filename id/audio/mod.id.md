{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "file", "ekstensi", "format", "apa itu format file mod", "musik", "format file mod", "mod vs MP3", "spesifikasi format file mod "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file MOD dan API yang dapat membuat, mengonversi, dan membuka file MOD.",
  "title" :"MOD - File Modul Musik",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## Apa itu file MOD?
File dengan ekstensi .mod adalah file modul musik yang dibuat menggunakan format modul musik standar, yang didasarkan pada **format modul Amiga** yang dikembangkan oleh Karsten Obarski dan dirilis dengan perangkat lunak **Ultimate Soundtracker** untuk Commodore Sistem amiga. Mirip dengan file [MIDI](/id/audio/mid/), file ini terdiri dari pola not dan sampel suara, yang mewakili instrumen berbeda yang dimainkan ulang sesuai dengan not. File MOD terutama digunakan dalam video game sebagai musik latar dan dalam subkultur seni komputer **demoscene**.

## Format File MOD

MOD adalah format file komputer yang menggunakan fungsi dasarnya untuk mewakili musik, dan itu adalah format file modul pertama. File MOD menggunakan ekstensi file .mod, kecuali pada **Amiga** yang membaca header file untuk menentukan tipe file, sehingga tidak bergantung pada ekstensi nama file. File MOD terdiri dari satu set berbagai instrumen dalam bentuk sampel, sejumlah pola yang menentukan bagaimana dan kapan sampel akan dimainkan, dan daftar pola apa yang dimainkan dalam urutan apa.

### Spesifikasi Format File MOD

Pola file MOD sebenarnya dirancang dalam antarmuka pengguna sequencer sebagai tabel dengan satu kolom per saluran, Jadi tabel ini memiliki empat kolom (satu untuk setiap saluran perangkat keras Amiga. Setiap kolom memiliki 64 baris).

Sel dalam tabel dapat menyebabkan salah satu tindakan berikut terjadi pada saluran kolomnya saat waktu barisnya tercapai:

- Mulai instrumen memainkan nada baru di saluran ini pada volume tertentu, kemungkinan dengan efek khusus yang diterapkan padanya
- Ubah volume atau efek khusus yang diterapkan pada catatan saat ini
- Ubah aliran pola; melompat ke posisi lagu atau pola tertentu atau loop di dalam pola
- Tidak melakukan apapun; not apa pun yang diputar di saluran ini akan terus diputar

Instrumen adalah sampel tunggal bersama dengan spesifikasi opsional yang bagian sampelnya dapat diulang untuk menghasilkan nada yang solid.

### Waktu
Kerangka waktu minimum adalah 0,02 detik dalam file MOD asli, atau interval "pengosongan vertikal" (VSync), karena perangkat lunak asli menggunakan pengaturan waktu VSync monitor yang berjalan pada 50 Hz (untuk PAL) atau 60 Hz (untuk NTSC) untuk pengaturan waktu.

## Referensi

* [MOD (format file) - Oleh Wikipedia](https://en.wikipedia.org/wiki/MOD_(file_format))

