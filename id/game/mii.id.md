{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file MGX Age of Empires 2 Expansion Replay dan API yang dapat membuat dan membuka file MGX.",
  "title" : "File MII - Format File Avatar Virtual Wii",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-id",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## Apa itu file MII?

File MII adalah format file avatar virtual yang digunakan untuk menyimpan avatar virtual di konsol game Nintendo Wii. File-file ini berisi informasi seperti tampilan avatar, gerakan, dan animasi. Mereka dapat digunakan dalam permainan, aplikasi jejaring sosial, dan perangkat lunak lain di Wii. File MII juga berisi fitur lain tentang avatar seperti jenis kelamin, warna rambut, warna kulit, fitur wajah, dan jenis mata.

Anda dapat membuka file MII menggunakan [My Avatar Editor](https://rc24.xyz/goodies/mii/).

## Format Berkas MII

Format file MII ditentukan secara rinci di [Wii Brew](https://wiibrew.org/wiki/Mii_data). String dalam file MII disimpan dalam format Unicode (UTF-16), big-endian.

### Blokir MI

Data file MII disimpan di Wiimote dalam dua blok. Setiap blok panjangnya 750 byte, dengan CRC 2 byte, sehingga totalnya menjadi 752 byte. Setiap blok dimulai dengan nilai 4-byte ('RNCD') yang tampaknya merupakan angka ajaib untuk format file MII.

## Bagaimana Cara Membuat File MII?

Ada beberapa cara berbeda untuk membuat avatar untuk Nintendo Wii:

1. `Menggunakan saluran Mii bawaan di Wii:` Saluran ini memungkinkan Anda membuat avatar khusus menggunakan berbagai alat, termasuk fitur wajah, bentuk tubuh, dan pakaian. Setelah Anda membuat avatar, Anda dapat menyimpannya sebagai file Mii dan menggunakannya dalam permainan dan perangkat lunak lain di Wii.

1. `Menggunakan aplikasi Mii Maker di Nintendo 3DS:` Aplikasi Mii Maker memungkinkan Anda membuat avatar khusus menggunakan layar sentuh dan kamera di Nintendo 3DS Anda. Setelah Anda membuat avatar, Anda dapat menyimpannya sebagai file Mii dan mentransfernya ke Wii melalui koneksi nirkabel.

1. `Menggunakan perangkat lunak pihak ketiga:` Beberapa pengembang telah membuat perangkat lunak yang memungkinkan Anda membuat avatar khusus untuk Wii. Perangkat lunak ini biasanya dirancang untuk digunakan pada komputer dan mungkin memerlukan langkah tambahan untuk mentransfer avatar ke Wii Anda.

1. `Menggunakan avatar siap pakai:` Beberapa game dan perangkat lunak lain di Wii mungkin dilengkapi dengan avatar siap pakai yang dapat Anda gunakan.

Dalam semua kasus, Anda harus memiliki akun Nintendo untuk membuat dan menyimpan avatar Anda di Wii.

## Referensi

* [Editor Avatar Saya](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)


