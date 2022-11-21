{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "file", "ekstensi", "format", "apa itu file cda", "musik", "format file cda", "spesifikasi format file cda"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file CDA dan API yang dapat membuat, mengonversi, dan membuka file CDA.",
  "title" :"CDA - File Pintasan Trek Audio CD",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Apa itu file CDA?

File dengan ekstensi .cda adalah file rintisan kecil yang dihasilkan oleh Microsoft Windows untuk setiap trek audio pada CD audio. File-file ini berisi informasi khas seperti waktu trek dan pintasan Windows yang memungkinkan pengguna mengakses trek audio tertentu. File CDA bukan musik, tetapi menunjuk ke file musik yang ada di suatu tempat di penyimpanan. Kita bisa menyebutnya sebagai shortcut file audio yang terletak di CD.

## Format File CDA

Format file CDA digunakan untuk memberi tahu komputer file audio mana yang akan diputar di CD. Jadi, file CDA menjadi tidak berguna dipisahkan dari CD yang diwakilinya. File CDA umumnya dianggap sebagai sumber daya RIFF. Hanya ada satu potongan yang diberi nama "CDDA" dan hanya berisi satu blok data yang disebut "FMT" dalam versi file .cda saat ini. Blok ini panjangnya 24 byte. Pengidentifikasi yang dibuat oleh Windows digunakan oleh drive CD terkait Windows 95 dan Windows 98 dan pemutarnya tidak dapat terhubung ke FreeDB atau CDDB. Agar dapat menampilkan judul lagu dan nama artis, Anda harus memasukkan informasi ini secara manual ke dalam file cdplayer.ini.

### Organisasi file CDA

Tabel berikut menampilkan informasi tentang offset tipikal:
| mengimbangi | panjang | konten |
---|---|---|
| 0x00 | 4 | 4 karakter ASCII "RIFF" |
| 0x04 | 4 | ukuran potongan berikut: selalu 36 (44 - 8), pada 4 byte (urutan Intel) |
| 0x08 | 4 | pengidentifikasi potongan: 4 karakter ASCII "CDDA" |
| 0x0C | 4 | 3 karakter ASCII "fmt" diikuti dengan spasi |
| 0x10 | 4 | panjang potongan: selalu 24, pada 4 byte (urutan Intel) |
| 0x14 | 2 | versi format CD, pada 2 byte (urutan Intel). Pada Mei 2006, selalu sama dengan 1. |
| 0x016 | 2 | nomor rentang, pada 2 byte (urutan Intel). Lagu pertama memiliki nomor 1. |
| 0x18 | 4 | pengidentifikasi dihitung oleh Windows untuk cdplayer.exe. |
| 0x1c | 4 | range offset, dalam jumlah frame (urutan Intel) |
| 0x20 | 4 | durasi trek, jumlah frame (urutan Intel) |
| 0x24 | 1 | posisi rentang: bingkai |
| 0x25 | 1 | posisi jangkauan: detik |
| 0x26 | 1 | posisi jangkauan: menit |
| 0x27 | 1 | byte nol (nilai biner 0) |
| 0x28 | 1 | durasi trek: frame |
| 0x29 | 1 | durasi trek: detik |
| 0x2a | 1 | durasi trek: menit |
| 0x2b | 1 | byte nol (nilai biner 0) |

## Referensi

* [file .cda - Oleh Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

