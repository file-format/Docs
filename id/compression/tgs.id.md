{
  "date" : "2019-10-11",
  "keywords" :[ "file tgs", "format file tgs", "apa itu file tgs", "file", "contoh tgs", "ekstensi file tgs", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Format File Stiker Animasi Telegram",
  "description":"Pelajari tentang format file TGS dan API yang dapat membuat dan membuka file TGS.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Apa itu file TGS?

File dengan ekstensi .tgs adalah file stiker animasi yang diperkenalkan oleh layanan perpesanan lintas platform, [Telegram](https://core.telegram.org/stickers#animated-stickers). Stiker animasi digunakan oleh pengguna aplikasi perpesanan untuk mengirim konten yang lebih disempurnakan dan hidup dalam pesan, tidak seperti grafik statis yang berupa gambar diam. Telegram awalnya menggunakan format file [WEBP](/id/image/webp/) untuk stiker gambar diam. Format file TGS dapat menyimpan data animasi dengan resolusi lebih tinggi dan ukuran file lebih kecil dibandingkan dengan stiker WEBP statis. File TGS dapat dibuka menggunakan aplikasi seperti Telegram, 7-zip, Apple Archive Utility, dan Corel WinZip.

## Format File TGS

Telegram memperkenalkan format file TGS pada Juli 2019 berdasarkan perpustakaan Lottie. File TGS terdiri dari teks [JSON](/id/web/json/) yang diekspor dari animasi di Adobe After Effects. Teks JSON yang diekspor dikompresi menggunakan kompresi gzip yang mengurangi ukuran file. Informasi JSON tentang file teks disimpan dalam file teks yang menjadi dasar dari tingkat kompresi yang tinggi.

### Spesifikasi Stiker TGS

Format file TGS memberlakukan batasan tertentu pada pembuatan stiker animasi TGS. File animasi TGS:

* Ukuran stiker/kanvas harus 512х512 piksel.
* Objek stiker tidak boleh keluar dari kanvas.
* Durasi animasi tidak boleh lebih dari 3 detik.
* Semua animasi harus diulang.
* Ukuran stiker tidak boleh melebihi 64 KB setelah dirender di Bodymovin.
* Semua animasi harus berjalan pada 60 Bingkai Per Detik.

### Contoh Teks JSON TGS

Contoh stiker animasi, saat dibuka ritsletingnya, berisi konten teks JSON berikut.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Referensi ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

