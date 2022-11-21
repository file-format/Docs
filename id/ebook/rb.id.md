{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "perangkat eBuku Rocket Nuvo Media", "file", "ekstensi", "format", "eBuku" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file RB untuk perangkat eBuku Rocket Nuvo Media dan API yang dapat membuat dan membuka file RB.",
  "title" :"RB - File eBuku Roket",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Apa itu file RB?

File dengan ekstensi .rb menyimpan konten eBook Rocket. eBuku Rocket sebenarnya adalah perangkat yang dibuat oleh Nuvo Media; mereka merilis perangkat ini pada tahun 1998. Walaupun Rocket eBook mampu menampilkan gambar, namun hanya dalam tampilan hitam putih. Ini memiliki layar 106 dpi atau 480 x 320 piksel pada layar sentuh 4,5 x 3 inci. eBuku Rocket terhubung ke komputer melalui koneksi port serial untuk mengunduh eBuku dalam format file RB. File RB mampu menggunakan DRM tetapi teknologi ini tidak digunakan di eBuku modern. File RB biasanya berisi file HTML dengan gambar dan file pseudo-OPF dengan semua metadata (.info).

## Spesifikasi Teknis Format File RB ##

Angka ajaib (dalam hex) muncul di 4 byte pertama file: B0 0C B0 0C.

Tampaknya dua byte berikutnya adalah nomor versi, seperti "02 00", yang berarti versi mayor 2 dan versi minor 0.

Empat byte berikutnya berisi teks "NUVO", diikuti oleh 4 byte 00h.

4-byte berikutnya adalah tanggal pembuatan buku, disandikan sebagai int16. Ini menempatkan kita pada offset 0Eh. Versi lama ORocketLibrary menyandikan nilai penuh tahun (yaitu, 1999 adalah "CF 07", 2000 adalah "D0 07"). Pada versi terbaru, tm_year disimpan kata demi kata, yaitu 100 untuk tahun 2000 ("64 00"). Setelah tahun muncul int8 yang mewakili angka bulan 1-relatif, dan int8 yang mewakili hari dalam sebulan.

6 byte berikutnya adalah 00h. Untuk pengaturan waktu, ini dapat dipesan.

Offset absolut dari "Daftar Isi" dimuat dalam int32 dengan offset 18 jam.

Setelah ini adalah int32 yang berisi panjang file .rb. Ini digunakan untuk menentukan apakah file sudah lengkap atau belum.

Seluruh potongan byte ini (20 jam hingga 128 jam) tampaknya hanya dibutuhkan oleh judul yang dienkripsi. Dalam judul yang tidak dienkripsi, nilainya selalu nol.

Dalam kebanyakan kasus, daftar isi mengikuti (pada offset 128). Ini dimulai dengan hitungan int32 dari jumlah entri "halaman" (bagian file .rb) di ToC. Setiap entri terdiri dari nama (zero-padded hingga 32 byte), diikuti oleh 3 int32: panjang segmen data, posisi dalam file .rb, dan flag untuk entri ini. Saat ini, nilai yang diketahui adalah: 1 (terenkripsi), 2 (halaman informasi), dan 8 (kempis). Semua nama disesuaikan, seperlunya, untuk memastikan semuanya unik.

## Referensi

* [E-Reader - Oleh MobileRead](https://en.wikipedia.org/wiki/E-reader)

