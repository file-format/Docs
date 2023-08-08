{
  "date" : "2021-04-08",
  "keywords" :[ "file lz4", "format file lz4", "apa itu file lz4", "file", "contoh lz4", "ekstensi file lz4", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Berkas Terkompresi LZ4 - LZ4",
  "description":"Pelajari tentang format file LBR dan API yang dapat membuat dan membuka file LZ4.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Apa itu file LZ4?

File dengan ekstensi .lz4 adalah file arsip terkompresi yang dibuat dengan aplikasi/utilitas yang mendukung kompresi [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)). Algoritma LZ4 berfokus pada trade-off antara kecepatan dan rasio kompresi. Arsip LZ4 terkompresi dapat dibuat menggunakan utilitas baris perintah LZ4 dan dapat didekompresi menggunakan yang sama.

## Format File LZ4

Format file LZ4, berdasarkan algoritme kompresi LZ4, tidak bergantung pada jenis CPU, sistem operasi, sistem file, dan rangkaian karakter. Sangat cocok untuk kompresi file dan kompresi streaming menggunakan algoritma LZ4. Implementasi awal format LZ4 dilakukan dalam bahasa [C](/id/programming/c/) oleh Yann Collet pada tahun 2011 dan tersedia untuk referensi developer di [Github](https://github.com/lz4/lz4) .

### Format Bingkai LZ4

Struktur umum format file LZ4 adalah seperti yang ditunjukkan di bawah ini.

|MagicNb|F. Deskriptor| Blokir|(...)|Tanda Akhir |C. Checksum|
---|---|---|---|---|---|
|4 byte| 3-15 byte||| 4 byte| 0-4 byte|

#### Angka Ajaib

4 Byte, format Little endian. Nilai : 0x184D2204

#### Deskripsi Bingkai

Deskriptor frame terdiri dari 3 t0 15 byte dan merupakan bagian terpenting dari spesifikasi. Bersama-sama, bidang Magic_Number dan Frame_Descriptor disebut sebagai LZ4 Frame Header, dan ukurannya bervariasi antara 7 dan 19 byte. Itu seperti yang ditunjukkan di bawah ini.

|FLG| BD| (Ukuran Konten)| (ID kamus)| HC|
---|---|---|---|---|
|1 byte| 1 byte| 0 - 8 byte| 0 - 4 byte| 1 byte|

#### Blok Data

Setiap blok data mengikuti urutan berikut.

|Ukuran Blok| data| (Blokir Checksum)|
---|---|---|
|4 byte| |0 - 4 byte|

#### Tanda Akhir

Aliran blok berakhir ketika blok data terakhir diikuti oleh nilai 32-bit 0x00000000.

#### Pemeriksaan Konten

Content_Checksum memverifikasi validitas konten yang didekodekan dengan benar dan dilakukan menggunakan hasil algoritma xxHash-32. Ini memvalidasi hasil transmisi sukses dari semua blok dalam urutan yang benar dan tanpa kesalahan apapun.

## Referensi

* [Format Bingkai LZ4](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [Algoritma Kompresi LZ4 - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

