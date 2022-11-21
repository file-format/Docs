{
  "date" : "2021-09-08",
  "keywords" :[ "file rel", "format file rel", "apa itu file rel", "file", "contoh rel", "ekstensi file rel", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file REL dan API yang dapat membuat dan membuka file REL.",
  "title" :"REL - File Modul yang Dapat Dipindahkan",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Apa itu file REL?
File dengan ekstensi .rel dapat digunakan untuk berbagai keperluan. Oleh karena itu, dalam klasifikasi game dikenal sebagai file modul yang dapat dipindahkan yang digunakan oleh beberapa game Nintendo Wii, seperti Brawl, Super Smash Bros, dan Mario Kart Wii. Ini terdiri dari data gameplay, termasuk model karakter dan tahapan. File REL berfungsi serupa dengan file .DLL yang digunakan oleh Microsoft Windows.

## format file REL
Dalam format file REL, file dibagi menjadi beberapa bagian, dikelompokkan berdasarkan akses yang sama, misalnya data hanya baca di satu bagian, semua kode yang dapat dieksekusi ditempatkan di bagian lain, dll. File dimulai dengan bagian header, diikuti oleh:
- Tabel yang berisi info bagian.
- Data bagian.
- Informasi relokasi.

### Tajuk berkas
File dimulai dengan header hingga 0x4C byte:
| mengimbangi | Ukuran | Nama Bidang | Deskripsi |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Nomor identifikasi sewenang-wenang. Harus unik di antara semua REL yang digunakan oleh game. Tidak boleh 0. |
| 0x04 | 4 | berikutnya | Pointer ke modul berikutnya, diisi saat runtime. |
| 0x08 | 4 | sebelumnya | Pointer ke modul sebelumnya, diisi saat runtime. |
| 0x0c | 4 | numSections | Jumlah bagian dalam file. |
| 0x10 | 4 | bagianInfoOffset | Offset ke awal tabel bagian. |
| 0x14 | 4 | namaOffset | Offset ke string ASCII yang berisi nama modul. Mungkin NULL. Relatif terhadap awal file REL. |
| 0x18 | 4 | namaUkuran | Ukuran nama modul dalam byte. |
| 0x1c | 4 | versi | Nomor versi format file REL. |
| 0x20 | 4 | ukuran bss | Ukuran bagian '.bss'. |
| 0x24 | 4 | relOffset | Offset ke meja relokasi. |
| 0x28 | 4 | impOffset | Offset ke tabel imp. |
| 0x2c | 4 | impSize | Ukuran tabel imp dalam byte. |
| 0x30 | 1 | bagian prolog | Indeks ke tabel bagian yang terkait dengan prolog. Lewati jika kolom ini adalah 0. |
| 0x31 | 1 | bagian epilog | Indeks ke dalam tabel bagian yang terkait dengan epilog. Lewati jika kolom ini adalah 0. |
| 0x32 | 1 | Bagian yang belum terselesaikan | Indeks ke tabel bagian yang relatif belum terselesaikan. Lewati jika kolom ini adalah 0. |
| 0x33 | 1 | Bagian bss | Indeks ke tabel bagian yang relatif terhadap bss. Diisi saat runtime! |
| 0x34 | 4 | prolog | Offset ke bagian tertentu dari fungsi _prolog. |
| 0x38 | 4 | epilog | Offset ke bagian tertentu dari fungsi _epilog. |
| 0x3c | 4 | belum terselesaikan | Offset ke bagian tertentu dari fungsi _unresolved. |
| 0x40 | 4 | menyelaraskan | Versi ≥ 2 saja. Kendala keselarasan pada semua bagian, dinyatakan sebagai pangkat 2. |
| 0x44 | 4 | bssAlign | Versi ≥ 2 saja. Batasan penyelarasan pada semua bagian '.bss', dinyatakan sebagai pangkat 2. |
| 0x48 | 4 | ukuran fix | Versi ≥ 3 saja. Jika REL ditautkan dengan OSLinkFixed (bukan OSLink), spasi setelah alamat ini dapat digunakan untuk tujuan lain (seperti BSS). |

### Tabel Info Bagian
Tabel info bagian berisi entri **numSections** dengan panjang masing-masing 0x8 byte:
| mengimbangi | Ukuran | Deskripsi |
-------|------------|-------------|
| 0x0 | 30 bit | Offset dari awal REL ke bagian. Jika ini nol, bagian tersebut adalah bagian yang tidak diinisialisasi (mis. .bss). |
| 0x3,6 | 1 bit | Tidak dikenal. |
| 0x3,7 | 1 bit | Bendera yang dapat dieksekusi; jika ini adalah 1 bagian dapat dieksekusi. |
| 0x4 | 4 | Panjang bagian dalam byte. Jika ini nol, entri ini dilewati. |
| 0x8 | Entri berikutnya | Entri berikutnya |

### Data Relokasi
Data relokasi adalah satu atau lebih daftar struktur 0x8 byte. Akhir dari setiap daftar ditandai dengan kode tipe khusus 203:
| mengimbangi | Nama | Ukuran | Deskripsi |
-------|------------|------------|-----|
| 0x0 | mengimbangi | 2 | Offset dalam byte dari relokasi sebelumnya ke relokasi ini. Jika ini adalah relokasi pertama di bagian tersebut, ini relatif terhadap awal bagian tersebut. |
| 0x2 | ketik | 1 | Jenis relokasi. Dijelaskan di bawah ini. |
| 0x3 | bagian | 1 | Bagian simbol yang akan dipindahkan. Untuk tipe relokasi khusus 202, ini adalah nomor bagian dalam file ini yang berlaku untuk entri relokasi berikut. |
| 0x4 | tambahkan | 4 | Offset dalam byte simbol yang akan dipindahkan, relatif terhadap awal bagiannya. Ini adalah alamat absolut sebagai gantinya untuk relokasi terhadap main.dol. |
| 0x8 | Entri berikutnya | Entri berikutnya | Entri berikutnya |


 




## Referensi


* [Format Modul Objek yang Dapat Dipindahkan](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


