{
  "date" : "2021-10-20",
  "keywords" :[ "file sfar", "format file sfar", "apa itu file sfar", "file", "contoh sfar", "Ekstensi File Mass Effect 3 DLC", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file SFAR Mass Effect 3 dan API yang dapat membuat dan membuka file SFAR.",
  "title" :"SFAR - Berkas DLC Mass Effect 3",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Apa itu file SFAR?

File dengan ekstensi .sfar adalah file data game yang digunakan oleh Mass Effect 3 untuk menyimpan DLC (konten yang dapat diunduh) dalam arsip berpemilik terkompresi. Mass Effect 3 adalah game yang dibuat oleh Electronic Arts, sebuah perusahaan pengembang game utama. Konten DLC yang disimpan dalam file SFAR digunakan untuk memperluas game dengan konten dan fitur tambahan.

## Format File SFAR - Informasi Lebih Lanjut

File SFAR disimpan/disimpan sebagai file arsip terkompresi dalam format file biner. Ini menggunakan algoritme kompresi LZX dan LZMA untuk mengompresi konten. File SFAR dapat dibuka menggunakan Editor DLC yang dikemas dengan ME3 Explorer. Selain SFAR, DLC Editor dapat mengekstrak file game lain seperti [PCC](/id/game/pcc/).

## Spesifikasi Format File SFAR

File SFAR dibagi menjadi empat bagian utama berikut.

### Tajuk SFAR

SFF Header berisi informasi tentang berbagai potongan yang terdiri dari file.

### Tabel Berkas SFAR

Tabel File SFAR berisi daftar entri file di mana setiap entri panjangnya 30 byte.

### Tabel Ukuran Balok

Ukuran Blok berisi banyak entri, di mana setiap entri panjangnya 2 bye. Nilai ini menentukan Ukuran Blok yang sesuai dengan entri di Tabel File.

### Blok

Potongan blok dalam file SFAR berisi data di dalam file SFAR.

## Referensi

* [Format File DLC SFAR - Penelitian](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

