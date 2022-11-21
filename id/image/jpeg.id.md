{
  "date" : "2019-11-25",
  "keywords" :[ "file jpeg", "format file jpeg", "apa itu file jpeg", "file", "contoh jpeg", "ekstensi file jpeg", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - Format Berkas Gambar",
  "description":"Pelajari tentang format file JPEG dan API yang dapat membuat dan membuka file JPEG.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## Apa itu file JPEG? ##

JPEG adalah jenis format gambar yang disimpan menggunakan metode kompresi lossy. Gambar keluaran, sebagai hasil kompresi, merupakan trade-off antara ukuran penyimpanan dan kualitas gambar. Pengguna dapat menyesuaikan tingkat kompresi untuk mencapai tingkat kualitas yang diinginkan sekaligus mengurangi ukuran penyimpanan. Kualitas gambar dapat diabaikan jika kompresi 10:1 diterapkan pada gambar. Semakin tinggi nilai kompresi, semakin tinggi penurunan kualitas gambar.

## Spesifikasi Format File ##

Format file gambar JPEG distandarisasi oleh Joint Photographic Experts Group dan karenanya diberi nama JPEG. Formatnya telah menjadi pilihan untuk menyimpan dan mengirimkan gambar fotografi di web. Hampir semua sistem Operasi sekarang memiliki penampil yang mendukung visualisasi gambar JPEG, yang sering juga disimpan dengan ekstensi JPG. Bahkan browser web mendukung visualisasi gambar JPEG. Sebelum masuk ke spesifikasi format file JPEG, keseluruhan proses langkah-langkah yang terlibat dalam pembuatan JPEG perlu disebutkan.

### Langkah Kompresi JPEG ###

**Transformasi:** Gambar warna diubah dari RGB menjadi gambar luminance/chrominance (Mata sensitif terhadap luminance, bukan chrominance, sehingga bagian chrominance dapat kehilangan banyak data dan dengan demikian dapat dikompresi secara tinggi.

**Down Sampling:** Down sampling dilakukan untuk komponen berwarna dan bukan untuk komponen pencahayaan .Down sampling dilakukan dengan rasio 2:1 secara horizontal dan 1:1 secara vertikal (2h 1 V). Dengan demikian ukuran gambar berkurang karena komponen 'y' tidak disentuh, tidak ada penurunan kualitas gambar yang nyata.

**Pengorganisasian dalam Grup:** Piksel dari setiap komponen warna diatur dalam kelompok berukuran 8x2 piksel yang disebut “unit data” jika jumlah baris atau kolom bukan kelipatan 8, baris paling bawah dan kolom paling kanan digandakan.

**Discrete Cosine Transformation:** Discrete Cosine Transform ( DCT) kemudian diterapkan ke setiap unit data untuk membuat peta 8×8 dari komponen yang diubah.DCT melibatkan beberapa kehilangan informasi karena keterbatasan presisi aritmatika komputer. Ini berarti bahwa meskipun tanpa peta akan ada penurunan kualitas gambar tetapi biasanya kecil.

**Kuantisasi:** Masing-masing dari 64 komponen yang diubah dalam unit data dibagi dengan angka terpisah yang disebut 'Koefisien Kuantisasi (QC)', lalu dibulatkan menjadi bilangan bulat. Di sinilah informasi hilang, QC besar menyebabkan lebih banyak kerugian. Secara umum, sebagian besar implementasi JPEG memungkinkan penggunaan tabel QC yang direkomendasikan oleh standar JPEG.

**Pengkodean:** 64 koefisien transformasi terkuantisasi (yang sekarang menjadi bilangan bulat) dari setiap unit data dikodekan menggunakan kombinasi pengkodean RLE dan Huffman.

**Menambahkan Header:** Langkah terakhir menambahkan header dan semua parameter JPEG yang digunakan dan mengeluarkan hasilnya.

Dekoder JPEG menggunakan langkah-langkah secara terbalik untuk menghasilkan gambar asli dari gambar terkompresi.

### Struktur Berkas ###

Gambar JPEG direpresentasikan sebagai urutan segmen di mana setiap segmen dimulai dengan penanda. Setiap penanda dimulai dengan byte 0xFF diikuti oleh penanda penanda untuk mewakili jenis penanda. Muatan yang diikuti oleh penanda berbeda sesuai jenis penanda. Jenis penanda JPEG umum adalah seperti yang tercantum di bawah ini:

|Nama Pendek|Byte|Muatan|Nama|Komentar
---|---|---|---|---|
|SOI|0xFF, 0xD8|tidak ada|Awal Gambar|
|S0F0|0xFF, 0xC0|ukuran variabel|Mulai Bingkai|
|S0F2|0xFF, 0xC2|ukuran variabel|Mulai dari Bingkai|
|DHT|0xFF, 0xC4|ukuran variabel|Tentukan Tabel Huffman|
|DQT|0xFF, 0xDB|ukuran variabel|Tentukan Tabel Kuantisasi|
|DRI|0xFF, 0xDD|4 byte|Tentukan Interval Mulai Ulang|
|SOS|0xFF, 0xDA|ukuran variabel|Mulai Pemindaian|
|RSTn|0xFF, 0xD//n//(/id//n//#0..7)|tidak ada|Mulai ulang|
|APPn|0xFF, 0xE//n//|ukuran variabel|Khusus aplikasi|
|COM|0xFF, 0xFE|ukuran variabel|Komentar|
|EOI|0xFF, 0xD9|tidak ada|Akhir Gambar|

Di dalam data berkode entropi, setelah setiap byte 0xFF, byte 0x00 disisipkan oleh pembuat enkode sebelum byte berikutnya, sehingga tampaknya tidak ada penanda yang tidak diinginkan, mencegah kesalahan pembingkaian. Decoder harus melewati 0x00 byte ini. Teknik ini, disebut [pengisian byte](https://en.wikipedia.org/wiki/Byte_stuffing) (lihat bagian spesifikasi JPEG F.1.2.3), hanya diterapkan pada data berkode entropi, bukan pada data payload marker . Namun perlu dicatat bahwa data berkode entropi memiliki beberapa penandanya sendiri; khususnya penanda Reset (0xD0 hingga 0xD7), yang digunakan untuk mengisolasi bagian independen dari data berkode entropi untuk memungkinkan decoding paralel, dan pembuat enkode bebas untuk memasukkan penanda Reset ini secara berkala (walaupun tidak semua pembuat enkode melakukan ini).

